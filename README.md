## Competition and selection

Since getting more involved with disease ecology, I've realized how inadequate the classic models of population genetics really are.  Population size is assumed to be constant and selection is purely Malthusian.  Variants can be placed along an axis with each variant fitter, healthier and more productive than the last.  The classic models are specified with a population size <i>N</i>, a rate of mutation <i>&mu;</i> and a selective effect of each new mutation <i>s</i>.  Under these assumptions, we can make a lot of analytic progress and quantify things like the probability that a particular mutation fixes in the population, the overall rate of adaptation, the expected level of genetic diversity, and so forth.
		
However, ecologists are not happy with this.  For them, the success or failure of a specific variant depends on its context, i.e. the characteristics of other members of the population or the composition of its greater biotic and abiotic environment.  A complete description of the selective process requires grounding selective forces in an ecological context and providing a mechanistic description of why a particular mutation is, at this moment, advantageous or deleterious. It’s not enough to say that a particular mutation grants higher 'fitness.' At heart, <i>selection</i> must be a dynamical consequence of <i>competition</i> among members of a population.
		
## Darwin's viewpoint

![](figures/darwin-tree.png)
				
This is only illustration in <i>On the Origin of Species</i> and it's remarkable in its depth of insight.  The <i>x</i>-axis here represents ecological variation.  "These species are supposed to resemble each other in unequal degrees."  Species A is more similar to species B than it is to species C and so forth.  Although we would expect the real landscape of ecological variation to be substantially more complex, this works to explain the concept.  Species that are close to one another on this axis compete for resources.  If species A becomes common then the growth rate of species B will suffer, but the growth rate of species K may be unaffected.
		
The <i>y</i>-axis represents time.  "The intervals between the horizontal lines in the diagram, may represent each a thousand generations; but it would have been better if each had represented ten thousand generations."  

As time proceeds, divergent species will be at an ecological advantage and thus "the most divergent of [the] variations will generally be preserved during the next thousand generations."  Here, it is not a process of one fitter variant replacing the last in succession.  Instead, we see continued ecological diversification and extinction of the less-competitive variants that remained in their historical niches.
		
## Updated figure

<script src="processing.min.js"></script>
<canvas datasrc="divergence.pjs" width="600" height="450">`Can't load canvas object`</canvas>

I've recapitulated Darwin's figure with modern technology.  Click to add an individual and start the simulation.  Press H to bring up a listing of additional commands.
		
Each genetic / ecological variant is represented as a circle.  The area of this circle is proportional to the number of individuals that possess this phenotype.  Variants can grow and decline in abundance and they can also mutate.  A mutation creates a new phenotype jittered slightly in position from that of the parent.  Lines show the mutational history connecting variants.
		
Additionally, the background is colored based on the level of competition that each ecological niche is experiencing, with shading getting lighter as competition increases.  You can see that variants are surrounded with a halo of ecological impact.  Variants experiencing more competition, i.e. on top of a lighter background, reproduce more slowly than variants undergoing less competition.
		
Thus, mutations push away from existing phenotypes will tend be successful and variants caught in the middle will tend to die out.  And the overall picture appears remarkable similar to Darwin's.
		
## Adaptive radiation and niche formation
		
If a new variant is added to the simulation with no other variants around to compete with it will initially increase to its carrying capacity, and then start to send off mutations.  These mutations will often reach areas with less competitive pressure and increase in abundance.  Thus, the peripheral variants tend to succeed, and their success pushes out more 'primitive' central variants that face competitive pressure from multiple angles.  This process resembles what happens during an adaptive radiation with rapid innovation into new ecological niches and the formation of new species.
		
However, if you let the simulation run for 5 minutes or so it will reach an equilibrium state in which the ecological space is neatly filled with variants at regular intervals.  The distribution of variants appears under-dispersed.  Once the system has reached this state, mutation becomes unfavorable and the ecological positions remain stable through time.  Thus, successive evolution builds a series of stable niches, each held in place by interactions with its surroundings.
