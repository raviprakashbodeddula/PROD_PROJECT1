node('dev')
{
   stage 'Get Artifact:'
   sh 'chmod 757 $WORKSPACE@script/*.sh'
   sh 'ssh bhagya@localhost mkdir -p $DEV_DESTINATION/'
   sh 'ssh bhagya@localhost chmod 757 $DEV_DESTINATION/'
   sh 'scp $WORKSPACE@script/*.sh bhagya@localhost:$DEV_DESTINATION/'

   stage 'Test:'
   sh 'ssh bhagya@localhost bash $DEV_DESTINATION/printn.sh 10'
   sh 'ssh bhagya@localhost bash $DEV_DESTINATION/tablen.sh 17'
   sh 'ssh bhagya@localhost bash $DEV_DESTINATION/primen.sh 10'
   sh 'ssh bhagya@localhost bash $DEV_DESTINATION/sort.sh 5 2 3 1 4'
   sh 'ssh bhagya@localhost bash $DEV_DESTINATION/compoundint.sh 100000 1y 12.4'
   sh 'ssh bhagya@localhost bash $DEV_DESTINATION/factorialn.sh 5'
   sh 'ssh bhagya@localhost bash $DEV_DESTINATION/a.sh 5'
   sh 'ssh bhagya@localhost bash $DEV_DESTINATION/b.sh'
   sh 'ssh bhagya@localhost bash $DEV_DESTINATION/c.sh'
   sh 'ssh bhagya@localhost bash $DEV_DESTINATION/d.sh'
}

node('test')
{
   stage 'Get Artifact:'
   sh 'chmod 757 $WORKSPACE@script/*.sh'
   sh 'ssh ravi@localhost mkdir -p $TEST_DESTINATION/'
   sh 'ssh ravi@localhost chmod 757 $TEST_DESTINATION/'
   sh 'scp $WORKSPACE@script/*.sh ravi@localhost:$TEST_DESTINATION/'

   stage 'Test:'
   sh 'ssh ravi@localhost bash $TEST_DESTINATION/printn.sh 10'
   sh 'ssh ravi@localhost bash $TEST_DESTINATION/tablen.sh 17'
   sh 'ssh ravi@localhost bash $TEST_DESTINATION/primen.sh 10'
   sh 'ssh ravi@localhost bash $TEST_DESTINATION/sort.sh 5 2 3 1 4'
   sh 'ssh ravi@localhost bash $TEST_DESTINATION/compoundint.sh 100000 1y 12.4'
   sh 'ssh ravi@localhost bash $TEST_DESTINATION/factorialn.sh 4'
   sh 'ssh ravi@localhost bash $TEST_DESTINATION/a.sh 5'
   sh 'ssh ravi@localhost bash $TEST_DESTINATION/b.sh'
   sh 'ssh ravi@localhost bash $TEST_DESTINATION/c.sh'
   sh 'ssh ravi@localhost bash $TEST_DESTINATION/d.sh'
}
