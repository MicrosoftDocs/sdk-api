---
UID: NE:strmif.__MIDL___MIDL_itf_strmif_0000_0132_0001
title: "__MIDL___MIDL_itf_strmif_0000_0132_0001"
author: windows-sdk-content
description: Indicates which user operation (UOP) commands are currently allowed by the DVD.
old-location: dshow\valid_uop_flag.htm
tech.root: DirectShow
ms.assetid: 419d3d5f-e775-438e-9754-0291df6a1ed7
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: UOP_FLAG_Pause_On, UOP_FLAG_PlayNext_Chapter, UOP_FLAG_PlayPrev_Or_Replay_Chapter, UOP_FLAG_Play_Backwards, UOP_FLAG_Play_Chapter, UOP_FLAG_Play_Chapter_Or_AtTime, UOP_FLAG_Play_Forwards, UOP_FLAG_Play_Title, UOP_FLAG_Play_Title_Or_AtTime, UOP_FLAG_Resume, UOP_FLAG_ReturnFromSubMenu, UOP_FLAG_Select_Angle, UOP_FLAG_Select_Audio_Stream, UOP_FLAG_Select_Karaoke_Audio_Presentation_Mode, UOP_FLAG_Select_Or_Activate_Button, UOP_FLAG_Select_SubPic_Stream, UOP_FLAG_Select_Video_Mode_Preference, UOP_FLAG_ShowMenu_Angle, UOP_FLAG_ShowMenu_Audio, UOP_FLAG_ShowMenu_Chapter, UOP_FLAG_ShowMenu_Root, UOP_FLAG_ShowMenu_SubPic, UOP_FLAG_ShowMenu_Title, UOP_FLAG_Still_Off, UOP_FLAG_Stop, VALID_UOP_FLAG, VALID_UOP_FLAG , VALID_UOP_FLAG enumeration [DirectShow], VALID_UOP_FLAGEnumeration, __MIDL___MIDL_itf_strmif_0000_0132_0001, dshow.valid_uop_flag, strmif/UOP_FLAG_Pause_On, strmif/UOP_FLAG_PlayNext_Chapter, strmif/UOP_FLAG_PlayPrev_Or_Replay_Chapter, strmif/UOP_FLAG_Play_Backwards, strmif/UOP_FLAG_Play_Chapter, strmif/UOP_FLAG_Play_Chapter_Or_AtTime, strmif/UOP_FLAG_Play_Forwards, strmif/UOP_FLAG_Play_Title, strmif/UOP_FLAG_Play_Title_Or_AtTime, strmif/UOP_FLAG_Resume, strmif/UOP_FLAG_ReturnFromSubMenu, strmif/UOP_FLAG_Select_Angle, strmif/UOP_FLAG_Select_Audio_Stream, strmif/UOP_FLAG_Select_Karaoke_Audio_Presentation_Mode, strmif/UOP_FLAG_Select_Or_Activate_Button, strmif/UOP_FLAG_Select_SubPic_Stream, strmif/UOP_FLAG_Select_Video_Mode_Preference, strmif/UOP_FLAG_ShowMenu_Angle, strmif/UOP_FLAG_ShowMenu_Audio, strmif/UOP_FLAG_ShowMenu_Chapter, strmif/UOP_FLAG_ShowMenu_Root, strmif/UOP_FLAG_ShowMenu_SubPic, strmif/UOP_FLAG_ShowMenu_Title, strmif/UOP_FLAG_Still_Off, strmif/UOP_FLAG_Stop, strmif/VALID_UOP_FLAG
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - VALID_UOP_FLAG
product: Windows
targetos: Windows
req.typenames: VALID_UOP_FLAG
req.redist: 
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
 

 

