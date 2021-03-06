d6-report
================

``` r
library("knitr")  
opts_knit$set(root.dir = "../")  
opts_chunk$set(echo = FALSE)  
```

## Introduction

The inspiration for this graph comes from personal experience. I have
played soccer since a very young age and I have been switched around in
team positions based on my changing physical attributes. I used to play
attack and as I grew older I moved into the defensive position. My coach
at that time said that the reason for the switch was because other
players were quicker for the position. I accepted the decision but that
made me wonder what physical attributes do I need to have inorder for me
to fit the Attack or Defence position.

## Requirement

This graph satisfies d6 requirements: \* Observations - 7491 \* Quant
variables - Attributes (Agility, Sprint Speed, Acceleration, Strength,
Reaction, Jumping , Balance, Stamina)

  - Quant variable (y) - Rating (20-100)

## Prose

In order to investigate this, I used the FIFA 19 player dataset. This
game has been around for a long time and has been tracking players for
almost 2 decades. It is the closest digital representation of player
attributes.

First, I looked at the mean of the overall. It seems that the mean ends
up being around 65. I also looked at how the data is distributed in the
dataset. I chose to take the all the players with an Overall greater
that 60. This ensures that we are looking at more developed players and
we also ensure we have about 75% of the dataset to avoid bias. Since we
are looking at physical attributes, I chose to take players over 18
since by then the body should have mostly developed (speaking in terms
of height etc). I chose to look at players in the Forward and Defensive
positions only. Since these 2 positions are the exact opposite, it was
worth looking into them. I did not take Midfielders because they have
mixed rolls on the pitch. There are players like CAM(Center Attacking
Mid) which has primarily attacking instructions and there are also
players like CDM(Central Defensive Mid) that supports the defense. Even
though they have certain roles, midfielders usually end up doing both
since they are the leeway between attack and defence. There were also a
bunch of other attributes I could have looked at but physical attributes
was the aim.

I created the following graph:

*Display 1: Shows comparison between physical attributes between attack
and defensive players* ![](../figures/d6-fifa-skewed.png)<!-- -->

**For some reason the graph does not show as i could not ggsave, I have
attached graph in the email and you can see it in the figures under the
named d6-fifa-skewed.png**

I coloured the different positions with red and blue. I feel they are
pretty distinct. It also maps with the viewers idea of attack (red) and
defence (blue). (Charlotte, [2018](#ref-RostLC2018b)). I did not make
the graph start at 0 since that would shrink it. The point of this is to
see what attributes are dominated by what category so I feel it does not
mislead. (Tufte, [1983](#ref-Tufte))

We can make the following observations:

  - Reactions : For this attribute there was no clear winner. We can wee
    that it is still a very mixed bag. However the range is from 45 to
    95 which is interesting to see. I looks like the player has to be
    above a certain level to attack or defend

  - Stamina : We can see that the stamina section is dominated by
    defenders. We can see blue lines flood the top as well as the
    bottom. We see that the lines are more dense on the top meaning,
    defenders end up having more stamina compared to attackers. Having
    said that, we also see a lot of lines on the bottom side of the
    section. This means that even though stamina is important, it is not
    a make or break factor for a defender.

  - Strength : This section is highy dominated by defenders. We see that
    it is extremely dense on top with the blue lines. We also see that
    the bottom section is filled with attackers. It is safe to say that
    this is a defining factor for defenders. It makes sense since they
    are involved with marking and blocking attackers.

  - Jumping : This section is again dominated by the defenders. We can
    see that the attackers have more leeway to get away with not having
    good jumping but defenders need to be good at it. This also makes
    sense since defending against corners requires the defenders to jump
    higher than the attacker. The price is higher to pay if you dont
    jump while defending than attacking.

  - Acceleration and Sprint Speed : Both these attributes represent how
    quick a player is. Both these categories show that attackers are
    more inclined to have high values for these categories. We see that
    the red lines become less and less dense as we fall below 70. The
    defenders occupy the bottom of the section. We can safely say that
    this is a very important attributes for attackers.

  - Balance : This category shows a dominance of attackers on the top
    section. The middle section is more mixed. However the bottom
    section is composed of mostly defenders meaning it is not as
    important for defenders than attackers.

  - Agility: This again is dominated by red on the top of the section
    and turns mostly blue by the time we get to the bottom. It looks
    like it is more important for attackers than defenders.

In conclusion, if you are an aspiring attacker. I would suggest you
focus on honing your Acceleration, Sprint Speed, Agility, Balance (in
order of importance)and If you want to be a defender, it makes more
sense to hone Strength, Jumping and Stamina.

Happy Playing\!

## References

<div id="refs" class="references">

<div id="ref-RostLC2018b">

Charlotte L (2018) What to consider when choosing colors for data
visualization. <https://blog.datawrapper.de/colors/>

</div>

<div id="ref-Tufte">

Tufte E (1983) The visual display of quantitative information. Graphics
Press, Cheshire, CT, 16–31
<https://www.edwardtufte.com/tufte/books_vdqi>

</div>

</div>
