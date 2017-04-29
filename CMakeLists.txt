cmake_minimum_required(VERSION 2.8.3)
project(roboy_comm)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS
  message_generation
  std_msgs
)

## Generate actions in the 'msg' folder
add_message_files(
  FILES
  EmotionMsg.msg
)

## Generate actions in the 'srv' folder
add_service_files(
  FILES
	Talk.srv
	recognition.srv
	seq2seq_eval.srv       
	srvCheckQuery.srv      
	srvShowPropertyValue.srv
	seq2seq_predict.srv    
	srvCreateInstance.srv  
	seq2seq_train.srv
	srvFindInstances.srv
	TextSpoken.srv
	ShowEmotion.srv 
	srvGetObject.srv    
	wakeup.srv
	srvAssertProperty.srv  
	srvSaveObject.srv
	srvCallQuery.srv    
	srvShowInstances.srv
	Movement.srv
	Yaw.srv

)

## Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  std_msgs
)

catkin_package(
 CATKIN_DEPENDS message_runtime std_msgs
)