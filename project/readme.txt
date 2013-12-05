How to compile: open the sln in the ../VisualStudio folder, then in visual studios put it in "Release" mode then go to the BUILD
tab and click on build solution. There will be warnings but they were from David Churchill's original UAlbertaBot.
Marvin.dll will be in the created release folder.

Changes:
		
Strategy Manager:

	added functions:
		-expandZerg()
		-getZergmutaliskBuildOrderGoal()
		-getZergZerglingBuildOrderGoal()
		-getZergLurkerBuildOrderGoal()
	added opening books:
		-ZergZerglingRush
		-ZergMutaRush
		-ZergLurkerRush
		
StarCraftData:
	
	added Zerg Buildings/upgrades/tech in void addActions(BWAPI::RACE & r)
	
MicroManager:
	added functions:
		-LurkerBurrow( BWAPI::Unit * rangedUnit ) const
		-LurkerUnBurrow( BWAPI::Unit * rangedUnit ) const
	modifyed smartAttackUnit to use Lurker Burrow/UnBurrow
	
ProductionManager:
	modifyed functions:
		//Made it so if your race is Zerg, avoid the BuildOrderSearch and go strait to queue
		//Fixed it so it will only try to build photon cannons if your Protoss
		-update() 
		//made it handle overlords better
		-detectBuildOrderDeadlock()