---
UID: NS:strmif.tagDVD_HMSF_TIMECODE
title: DVD_HMSF_TIMECODE (strmif.h)
author: windows-sdk-content
description: The DVD_HMSF_TIMECODE structure gives the hours, minutes, seconds, and frames in a DVD timecode.
old-location: dshow\dvd_hmsf_timecode.htm
tech.root: DirectShow
ms.assetid: 8f2990f6-a8f5-4b16-ae30-d51ea55496ea
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DVD_HMSF_TIMECODE, DVD_HMSF_TIMECODE structure [DirectShow], DVD_HMSF_TIMECODEStructure, dshow.dvd_hmsf_timecode, strmif/DVD_HMSF_TIMECODE
ms.topic: struct
f1_keywords: 
 - "strmif/DVD_HMSF_TIMECODE"
dev_langs:
 - c++
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
 - DVD_HMSF_TIMECODE
targetos: Windows
req.typenames: DVD_HMSF_TIMECODE
req.redist: 
ms.custom: 19H1
---

# DVD_HMSF_TIMECODE structure


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



A <code>DVD_HMSF_TIMECODE</code> structure is used in various <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> and <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2</a> methods. A <code>DVD_HMSF_TIMECODE</code> structure can be cast to or from a <b>ULONG</b> value. This means that if you need to use the old BCD time format for backward compatibility, you can do so in place of a <code>DVD_HMSF_TIMECODE</code> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>
 

 

