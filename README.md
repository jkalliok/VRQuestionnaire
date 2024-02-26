# VRQuestionnaire
Unity assets to run questionnaire in VR

#Requirements
To use this in your project you have to be using OpenXR and OpenXR Interaction Toolkit plugins.

#Usage
If you want to use the basic SSQ-questionnaire you have to do:

When you want the user to start filling the questionnaire you need to open the SSQ_Scene using LoadSceneMode.Additive
After the scene have loaded there are few things you need to do:
- Set the basePath and userID values in QSystem script. These can be accessed from any script using static variables QSystem.basePath and QSystem.userID. The userID can also be changed by the experimenter in the GUI.
- Set the receiver in QSystem script. This can be accessed from any script using static variable QSystem.receiver. After the questionnaire is filled out and the researcher saves the questionnaire, it will call function called "QuestionnaireSaved" in the receiver gameObject. This can be used to know when to continue the project after the questionnaire
- After the participant has filled out the questionnaire, the experimenter needs to press the "Save Questionnaire"-button to save the results.

#Other
By default, the SSQ questionnaire results are written in single csv file containing field userID and fields for each of the choices in SSQ questionnaire. This can be changed by going to SSQ_Scene and changing the SingleFile variable from the QuestionnaireSystem Object.
The results are saved in "C:/Users/<username>/AppData/LocalLow/<ProjectName>/<basePath>/"

#NOTICE IMPORTANT
The script has not yet been used in any study. Before starting running, please make sure everything works and that the data is saved correctly
