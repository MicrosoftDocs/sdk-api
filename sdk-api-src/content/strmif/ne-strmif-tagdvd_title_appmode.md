---
UID: NE:strmif.tagDVD_TITLE_APPMODE
title: tagDVD_TITLE_APPMODE
author: windows-sdk-content
description: Indicates whether a DVD title is a karaoke title. This enumeration is a member of the DVD_TitleAttributes structure, which is filled when an application calls the IDvdInfo2::GetTitleAttributes method.
old-location: dshow\dvd_title_appmode.htm
old-project: DirectShow
ms.assetid: f0a12b00-89a5-4b70-9a78-519ae36d1bac
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: DVD_AppMode_Karaoke, DVD_AppMode_Not_Specified, DVD_AppMode_Other, DVD_TITLE_APPMODE, DVD_TITLE_APPMODE , DVD_TITLE_APPMODE enumeration [DirectShow], DVD_TITLE_APPMODEEnumeration, dshow.dvd_title_appmode, strmif/DVD_AppMode_Karaoke, strmif/DVD_AppMode_Not_Specified, strmif/DVD_AppMode_Other, strmif/DVD_TITLE_APPMODE, tagDVD_TITLE_APPMODE
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
tech.root: 
req.typenames: DVD_TITLE_APPMODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	strmif.h
api_name:
-	DVD_TITLE_APPMODE
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# tagDVD_TITLE_APPMODE enumeration


## -description



Indicates whether a DVD title is a karaoke title. This enumeration is a member of the <a href="https://msdn.microsoft.com/e80baf09-93b7-4285-ac9a-af72cae137de">DVD_TitleAttributes</a> structure, which is filled when an application calls the <a href="https://msdn.microsoft.com/4e901e14-9e98-4ca5-ae37-7a4564b187ab">IDvdInfo2::GetTitleAttributes</a> method.




## -enum-fields




### -field DVD_AppMode_Not_Specified

The disc does not provide any application mode information about this title.


### -field DVD_AppMode_Karaoke

Title contains karaoke content.


### -field DVD_AppMode_Other

Title contains a type of content that the <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator Filter</a> does not recognize, so the application should treat the title as a regular DVD-Video title.


## -remarks



When the DVD Navigator encounters a karaoke title on a disc, it goes into "karaoke mode" and informs the audio decoder. The decoder must respond by initially muting the three auxiliary channels. Applications can then selectively control the volume and mixing configuration of these channels using the karaoke-related methods in the <a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2</a> interface For more information, see <a href="https://msdn.microsoft.com/1a8d0f42-35b8-4743-9ae7-619b99936f76">Playing Karaoke Audio Streams</a>.




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>
 

 

