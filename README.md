## Viewplan

Viewplan is a Python script for generating telescope viewing plans for amateur astronomers. It lets you specify the time and location for the viewing, and various constraints on the target; it provides RA, declination, and other information for each target.

### Examples

You're near Boston, you want to start watching right away, light pollution is making 
it impossible to see faint clusters, but you wouldn't mind seeing some bright double 
stars.  

~~~
python viewplan.py --city Boston --start "in 15 minutes" --dsolimit 4 --stars --starlimit 1.8
Your viewing plan:
 viewing from 2015/6/7 05:45:26 (UTC)
 viewing from Boston
 including planets
 including interesting stars down to magnitude 1.8
 including nebulae and other DSOs down to magnitude 4.0
 limiting targets to altitudes between 20 and 70 degrees elevation

                Name        Azimuth       Altitude    Mag   Eyepc           Description 
--------------------  -------------  -------------  -----  ------  -------------------- 
              Alioth   313°55'37.3"    40°40'24.4"    1.8            visual double star
            Arcturus   262°05'47.8"    37°18'15.2"    0.2                 variable star
              Altair   136°30'00.5"    48°52'58.3"    0.9            visual double star
               Deneb    70°13'08.0"    61°23'05.9"    1.3            visual double star
    Andromeda Galaxy    51°55'55.5"    20°17'24.0"    3.5    45mm         spiral galaxy
              Saturn   212°51'44.0"    22°49'14.9"    0.1     3mm                planet
                Moon   132°09'15.4"    20°19'51.2"  -12.4     7mm                  moon
~~~

### Future Work

* Add an option to display RA and declination instead of altitude and azimuth.
* Add an option to display good candidate stars for alignment.
* Allow the user to specify what eyepiece focal lengths they have available.
* Sort the targets west-to-east so you can catch them before they set.
* Sort the targets to reduce total scope slew time while still working generally west-to-east, without going full Traveling Salesman.
* Add an end time option, allowing targets to be considered which are below the eastern horizon at the start of the plan.


