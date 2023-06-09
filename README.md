Download Link: https://assignmentchef.com/product/solved-cs2124-homework-7-inheritance
<br>
<strong>hw07: Inheritance</strong>

<strong>Update!</strong>

<ul>

 <li>Yes, lords can fire protectors.</li>

 <li>Also those with strength to fight now have their own battle cry. This latter change may make your code easier.</li>

 <li>You may (or may not) find a description added to the end of this assignment with regards to a “framework”, helpful in understanding the structure of your battle method and why you only need one..</li>

</ul>

<strong>Focus</strong>

<ul>

 <li>Inheritance</li>

</ul>

<strong>Problem:</strong>

We want to again extend our game of Warriors and Nobles

It turns out that there is more than one type of Noble. And in fact Warriors aren’t the only people they can hire to do their fighting. There is magic in the land! Life (and death) are otherwise fairly similar. Nobles are still the only ones who go around declaring war upon each other.

<strong>Nobles</strong>

Nobles come in two varieties with rather fancy sounding titles:

<ul>

 <li>Those Who are Lords of the Land</li>

 <li>Those With Strength to Fight</li>

</ul>

<strong>Those Who are Lords of the Land</strong>

Those Who are Lords of the Land have no strength of their own but are able to fight using the strength and skill of their army.

Thus these are the people whom we knew as Nobles in past assignments.

A Lord’s army consist of Protectors. When a Lord goes into battle with another Noble, <u>each of the Lord’s Protectors will </u><em><u>defend</u></em><u> him</u> in a way described below, under Protectors.

The Lord will win or lose depending on whether the total combined strength of his army is more or less than the strength of the opposing Noble. The strengths of each of his Protectors will be effected by the battle in the same manner as in prior assignments with the Noble’s army.

The idea of “defending” is new to this assignment.

Lords can both <u>hire and fire</u> Protectors. When a Protector is fired, the others in the army close the gap between them, so that the Protectors maintain the same order they had before in the army. (Wouldn’t want warriors having to run all about just because one of their comrades gets fired.)

<strong>Those With Strength to Fight</strong>

This type of Noble is rather different from those we have encountered before. They actually do their own fighting!!!

When doing battle, one with strength to fight will yell “UGH!!!”, this being the battle cry handed down to them from the famous Barbarian, Conan. They hope that this will help them in defending themselves.

Furthermore, those With Strength to Fight fight using <em>only their own</em> strength. They <u>do not hire anyone to fight for them and therefore do not have an army</u>. They are born with a certain strength and they have no hope, neither through magic nor excessive exercise, to ever again increase their strength. Alas, our poor fighters will eventually have no strength left with which to fight and thus they shall meet their final demise.

<strong>Protectors</strong>

Who are these Protectors that defend Lords to the death?

<ul>

 <li>they are not Nobles!</li>

 <li>they are entities for hire with strength to defend. The amount of their strength set at birth.</li>

 <li>they are entities for hire that have names handed down from times of yore such as “QuessTar” and “VerTraahn”, sacred names given at birth.</li>

</ul>

[<strong>Clarification:</strong> Hm, there’s nothing you have to do about making sure that the names are spelled weirdly or any such. That’s just there to make the story line sound more exciting.]

Lords approach Protectors to attempt to engage the service of the Protector. A Lord asks of the Protector if they are at present hired to serve another Lord and if the Protector states that he is, no transaction can take place. However if the transaction can be made, it is – and the Protector is, from that moment onward, in the service of the Lord as defender.

[<strong>Clarification:</strong> All this so-called dialog simply comes down to is the Lord trying to hire the Protector and succeeding if it’s possible.]

In this land there are two kinds of Protectors:

<ul>

 <li>Wizards</li>

 <li>Warriors</li>

</ul>

They differ in their ways of defending!

This is the topic mentioned above that is new for this assigment in terms of how individual Protectors fight. In the past the only thing that mattered about one of our warrior’s was their strength. Now they acutally <em>do</em> something. Too bad we don’t also have animation!

Wizards state “POOF”. It is such a hard job to control the strength expended with magic!

There are, further, two kinds of Warriors whose strength is spent in much more known ways:

<ul>

 <li>Archers

  <ul>

   <li>who defend by stating “TWANG! <em>&lt;archer’s name&gt;</em>says: Take that in the name of my lord, __________” (whence he shouts the name of the lord he is sworn to defend)</li>

  </ul></li>

 <li>Swordsmen

  <ul>

   <li>who defend by stating “CLANG! <em>&lt;swordsman’s name&gt;</em>says: Take that in the name of my lord, __________” (whence he shouts the name of the lord he is sworn to defend)</li>

  </ul></li>

</ul>

Again, coders beware that your code do rightly enforce all these things about a Protector, be he Wizard, Archer or Swordsman.

<strong>Loss of Strength</strong>

Each entity with strength loses it in the same manor as described in prior assignments.

<strong>Death</strong>

It’s a sad topic, but one we do have to address.

<ul>

 <li>People die when they lose a battle, whether they are a Noble or a Protector.</li>

 <li>Lords who are dead are in no position to hire anyone. Any attempt by a dead Lord to hire someone will simple fail and the Protector will remain unhired.</li>

 <li>Similarly dead Protectors cannot be hired. Any attempt to hire the dead simple fails.</li>

 <li>However curiously, as has been seen before, Nobles can declare battle even though they are dead.</li>

 <li>A Protector who is dead, however, cannot fight and so will not have anything to say, even if his Lord does go into battle again.</li>

</ul>

<strong>A sample test file</strong>

/*  Your classes go here */




int main() {

Lord sam(“Sam”);

Archer samantha(“Samantha”, 200);

sam.hires(samantha);

Lord joe(“Joe”);

PersonWithStrengthToFight randy(“Randolf the Elder”, 250);

joe.battle(randy);

joe.battle(sam);

Lord janet(“Janet”);

Swordsman hardy(“TuckTuckTheHardy”, 100);

Swordsman stout(“TuckTuckTheStout”, 80);

janet.hires(hardy);

janet.hires(stout);

PersonWithStrengthToFight barclay(“Barclay the Bold”, 300);

janet.battle(barclay);

janet.hires(samantha);

Archer pethora(“Pethora”, 50);

Archer thora(“Thorapleth”, 60);

Wizard merlin(“Merlin”, 150);

janet.hires(pethora);

janet.hires(thora);

sam.hires(merlin);

janet.battle(barclay);

sam.battle(barclay);

joe.battle(barclay);

}

My output for the above test file is below.

Joe battles Randolf the Elder

Randolf the Elder defeats Joe

Joe battles Sam

He’s dead, Sam

Janet battles Barclay the Bold

CLANG!  TuckTuckTheHardy says: Take that in the name of my lord, Janet

CLANG!  TuckTuckTheStout says: Take that in the name of my lord, Janet

Barclay the Bold defeats Janet

Janet battles Barclay the Bold

He’s dead, Barclay the Bold

Sam battles Barclay the Bold

TWANG!  Samantha says: Take that in the name of my lord, Sam

POOF!

Sam defeats Barclay the Bold

Joe battles Barclay the Bold

Oh, NO!  They’re both dead!  Yuck!

<strong>The Focus of the Assignment</strong>

The <em>main</em> focus of the assignment is to do the inheritance correctly! Place any members as high in the heirarchy as possible, but only as high as makes sense. The Noble battle method should only be defined once, not once for each possible combination of Nobles. Make use of abstract methods / classes where appropriate.

<u>Cyclic association:</u> While not discussed above or demonstrated in the test code, all of the Protectors can quit, just as our Warriors were able to do previously.

<u>Separate compilation and namespaces:</u> Again, use separate compilation. You may, if you like, put all of the Protector types in one header / implementation pair, and the various Noble types in another pair. Or create a header / implementation pair for every class, as you like. Place all classes in the WarriorCraft namespace.

<u>Framework:</u> While we see that the different Nobles battle somewhat differently, really they are doing the same sequence of things, involving 1) determining their own strength, 2) either defending themselves or having their army defend them, and 3) winning or losing with the corresponding adjustment to their strength, and in the case of the Lords, the strengths of each of their Protectors. This is why we only need on battle method in the base class Noble as it can call on methods in the derived Noble classes to correctly handle each stage.