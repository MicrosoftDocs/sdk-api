---
UID: NF:segment.IMSVidXDSEvent.RatingChange
title: IMSVidXDSEvent::RatingChange
author: windows-sdk-content
description: The RatingChange method is called when the current rating changes.
old-location: mstv\imsvidxdsevent_ratingchange.htm
tech.root: MSTV
ms.assetid: 2832f99b-16e9-4c09-903d-8d89f2cc7715
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IMSVidXDSEvent interface [Microsoft TV Technologies],RatingChange method, IMSVidXDSEvent.RatingChange, IMSVidXDSEvent::RatingChange, IMSVidXDSEventRatingChange, RatingChange, RatingChange method [Microsoft TV Technologies], RatingChange method [Microsoft TV Technologies],IMSVidXDSEvent interface, mstv.imsvidxdsevent_ratingchange, segment/IMSVidXDSEvent::RatingChange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidXDSEvent.RatingChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidXDSEvent::RatingChange


## -description



<div class="alert"><b>Note</b>  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later.</div>
<div> </div>



The <b>RatingChange</b> method is called when the current rating changes.




## -parameters




### -param PrevRatingSystem [in]

The previous rating system, as an <a href="https://msdn.microsoft.com/646927ad-569a-4484-a3ce-6d121210b6be">EnTvRat_System</a> enumeration type.


### -param PrevLevel [in]

The previous rating level, as an <a href="https://msdn.microsoft.com/f96a8f1a-d8e2-4976-92e3-719f0039d2a8">EnTvRat_GenericLevel</a> enumeration type. The meaning of this value depends on the rating system.


### -param PrevAttributes [in]

The previous rating attributes. This value is a bitwise OR of flags from the <a href="https://msdn.microsoft.com/eb7f56c4-1d48-43f9-a691-c08aee3cd537">BfEnTvRat_GenericAttributes</a> enumeration. These flags specify content attributes, such as violence or adult language. Content attributes do not apply to all rating systems.


### -param NewRatingSystem [in]

The new rating system, as an <b>EnTvRat_System</b> enumeration type.


### -param NewLevel [in]

The new rating level, as an <b>EnTvRat_GenericLevel</b> enumeration type.


### -param NewAttributes [in]

Specifies the new rating attributes. This value is a bitwise OR of flags from the <b>BfEnTvRat_GenericAttributes</b> enumeration.


## -returns



Return S_OK or an error code.




## -see-also




<a href="https://msdn.microsoft.com/c89f378d-daa6-4e01-a087-6082d368585b">IMSVidXDSEvent Interface</a>
 

 

