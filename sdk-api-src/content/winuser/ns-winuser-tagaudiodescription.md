---
UID: NS:winuser.tagAUDIODESCRIPTION
title: tagAUDIODESCRIPTION
author: windows-sdk-content
description: Contains information associated with audio descriptions. This structure is used with the SystemParametersInfo function when the SPI_GETAUDIODESCRIPTION or SPI_SETAUDIODESCRIPTION action value is specified.
old-location: winmsg\audiodescription.htm
tech.root: winmsg
ms.assetid: 20eb48da-cd2b-4af8-b3a7-5ee3f39b1387
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: "*LPAUDIODESCRIPTION, AUDIODESCRIPTION, AUDIODESCRIPTION structure [Windows and Messages], LPAUDIODESCRIPTION, LPAUDIODESCRIPTION structure pointer [Windows and Messages], audiodescription_cpp, base.audiodescription, tagAUDIODESCRIPTION, winmsg.audiodescription, winui.audiodescription, winuser/AUDIODESCRIPTION, winuser/LPAUDIODESCRIPTION"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Winuser.h
api_name:
 - AUDIODESCRIPTION
product: Windows
targetos: Windows
req.typenames: AUDIODESCRIPTION, *LPAUDIODESCRIPTION
req.redist: 
---

# tagAUDIODESCRIPTION structure


## -description


Contains information associated with audio descriptions. This structure is used with the 
<a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a> function when the SPI_GETAUDIODESCRIPTION or SPI_SETAUDIODESCRIPTION action value is specified.


## -struct-fields




### -field cbSize

The size of the structure, in bytes. The caller must set this member to <code>sizeof(AUDIODESCRIPTION)</code>.


### -field Enabled

If this member is <b>TRUE</b>, audio descriptions are enabled; Otherwise, this member is <b>FALSE</b>.


### -field Locale

The locale identifier (LCID) of the language for the audio description. For more information, see 
       <a href="https://msdn.microsoft.com/8214c00d-4ec6-4597-8088-7819a160f0dc">Locales and Languages</a>.


## -remarks



To compile an application that uses this structure, define _WIN32_WINNT as 0x0600 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a>
 

 

