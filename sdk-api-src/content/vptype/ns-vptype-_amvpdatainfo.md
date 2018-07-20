---
UID: NS:vptype._AMVPDATAINFO
title: "_AMVPDATAINFO"
author: windows-sdk-content
description: The AMVPDATAINFO structure specifies the data-specific characteristics of the VP input stream.
old-location: dshow\amvpdatainfo.htm
old-project: DirectShow
ms.assetid: b71fc468-b0ba-4c75-b1db-b7802e598e96
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: "*LPAMVPDATAINFO, AMVPDATAINFO, AMVPDATAINFO structure [DirectShow], AMVPDATAINFOStructure, LPAMVPDATAINFO, LPAMVPDATAINFO structure pointer [DirectShow], _AMVPDATAINFO, dshow.amvpdatainfo, vptype/AMVPDATAINFO, vptype/LPAMVPDATAINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: vptype.h
req.include-header: 
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
req.typenames: AMVPDATAINFO, *LPAMVPDATAINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - vptype.h
api_name:
 - AMVPDATAINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _AMVPDATAINFO structure


## -description



The <b>AMVPDATAINFO</b> structure specifies the data-specific characteristics of the VP input stream.




## -struct-fields




### -field dwSize

Size of the structure, in bytes.


### -field dwMicrosecondsPerField

Time taken by each field.


### -field amvpDimInfo

Dimensional information.


### -field dwPictAspectRatioX

The X dimension of picture aspect ratio.


### -field dwPictAspectRatioY

The Y dimension of picture aspect ratio.


### -field bEnableDoubleClock

Video port should enable double clocking.


### -field bEnableVACT

Video port should use an external VACT signal.


### -field bDataIsInterlaced

Indicates that the signal is interlaced.


### -field lHalfLinesOdd

Number of half lines in the odd field.


### -field bFieldPolarityInverted

Video port should invert the field polarity.


### -field dwNumLinesInVREF

Number of lines of data in VREF.


### -field lHalfLinesEven

Number of half lines in the even field.


### -field dwReserved1

Reserved for future use.


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

