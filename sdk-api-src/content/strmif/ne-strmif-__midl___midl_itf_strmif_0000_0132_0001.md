---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# __MIDL___MIDL_itf_strmif_0000_0132_0001 enumeration


## -description



Indicates which user operation (UOP) commands are currently allowed by the DVD.




## -enum-fields




### -field UOP_FLAG_Play_Title_Or_AtTime


            Annex J commands: Time_Play, TimeSearch.
          


### -field UOP_FLAG_Play_Chapter


            Annex J commands: PTT_Play, PTT_Search.
          


### -field UOP_FLAG_Play_Title


            Annex J command: Title_Play.
          


### -field UOP_FLAG_Stop


            Annex J command: Stop.
          


### -field UOP_FLAG_ReturnFromSubMenu


            Annex J command: GoUp.
          


### -field UOP_FLAG_Play_Chapter_Or_AtTime


            Annex J commands: Time_Search, PTT_Search.
          


### -field UOP_FLAG_PlayPrev_Or_Replay_Chapter


            Annex J commands: PrevPG_Search, TopPG_Search.
          


### -field UOP_FLAG_PlayNext_Chapter


            Annex J command: NextPG_Search.
          


### -field UOP_FLAG_Play_Forwards


            Annex J command: Forward_Scan.
          


### -field UOP_FLAG_Play_Backwards


            Annex J command: Backward_Scan.
          


### -field UOP_FLAG_ShowMenu_Title


            Annex J command: Menu_Call(<i>Title</i>).
          


### -field UOP_FLAG_ShowMenu_Root


            Annex J command: Menu_Call(<i>Root</i>).
          


### -field UOP_FLAG_ShowMenu_SubPic


            Annex J command: Menu_Call(<i>Sub-picture</i>).
          


### -field UOP_FLAG_ShowMenu_Audio


            Annex J command: Menu_Call(<i>Audio</i>).
          


### -field UOP_FLAG_ShowMenu_Angle


            Annex J command: Menu_Call(<i>Angle</i>).
          


### -field UOP_FLAG_ShowMenu_Chapter


            Annex J command: Menu_Call(<i>PTT</i>).
          


### -field UOP_FLAG_Resume


            Annex J command: Resume.
          


### -field UOP_FLAG_Select_Or_Activate_Button


            Annex J commands: Upper_Button_Select, Lower_Button_Select, Left_Button_Select, Right_Button_Select, Button_Activate, Button_Select_And_Activate.
          


### -field UOP_FLAG_Still_Off


            Annex J command: Still_Off.
          


### -field UOP_FLAG_Pause_On


            Annex J command: Pause_On.
          


### -field UOP_FLAG_Select_Audio_Stream


            Annex J command: Audio_Stream_Change.
          


### -field UOP_FLAG_Select_SubPic_Stream


            Annex J command: Sub-picture_Stream_Change.
          


### -field UOP_FLAG_Select_Angle


            Annex J command : Angle_Change.
          


### -field UOP_FLAG_Select_Karaoke_Audio_Presentation_Mode


            Annex J command: Karaoke_Audio_Presentation_Mode_Change.
          


### -field UOP_FLAG_Select_Video_Mode_Preference


            Annex J command: Video_Presentation_Mode_Change.
          


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/71ae88f0-17ad-4530-b2e7-6a8155c14a97">IDvdInfo2::GetCurrentUOPS</a>
 

 

