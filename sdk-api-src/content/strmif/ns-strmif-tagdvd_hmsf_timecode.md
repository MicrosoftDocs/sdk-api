---
UID: NS:strmif.tagDVD_HMSF_TIMECODE
title: tagDVD_HMSF_TIMECODE
author: windows-sdk-content
description: The DVD_HMSF_TIMECODE structure gives the hours, minutes, seconds, and frames in a DVD timecode.
old-location: dshow\dvd_hmsf_timecode.htm
old-project: DirectShow
ms.assetid: 8f2990f6-a8f5-4b16-ae30-d51ea55496ea
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: DVD_HMSF_TIMECODE, DVD_HMSF_TIMECODE structure [DirectShow], DVD_HMSF_TIMECODEStructure, dshow.dvd_hmsf_timecode, strmif/DVD_HMSF_TIMECODE, tagDVD_HMSF_TIMECODE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: DVD_HMSF_TIMECODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DVD_HMSF_TIMECODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# tagDVD_HMSF_TIMECODE structure


## -description



The <code>DVD_HMSF_TIMECODE</code> structure gives the hours, minutes, seconds, and frames in a DVD timecode.




## -struct-fields




### -field bHours

Hours.


### -field bMinutes

Minutes.


### -field bSeconds

Seconds.


### -field bFrames

Frames.


## -remarks



A <code>DVD_HMSF_TIMECODE</code> structure is used in various <a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2</a> and <a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2</a> methods. A <code>DVD_HMSF_TIMECODE</code> structure can be cast to or from a <b>ULONG</b> value. This means that if you need to use the old BCD time format for backward compatibility, you can do so in place of a <code>DVD_HMSF_TIMECODE</code> structure.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

