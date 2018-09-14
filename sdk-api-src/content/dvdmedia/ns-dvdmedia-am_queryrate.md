---
UID: NS:dvdmedia.AM_QueryRate
title: AM_QueryRate
author: windows-sdk-content
description: The AM_QueryRate structure is used to query the decoder's maximum full-frame rate for forward and reverse playback.
old-location: dshow\am_queryrate.htm
tech.root: DirectShow
ms.assetid: a791f6ac-f415-4641-bac1-26db983a1ef7
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: AM_QueryRate, AM_QueryRate structure [DirectShow], AM_QueryRateStructure, dshow.am_queryrate, dvdmedia/AM_QueryRate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dvdmedia.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dvdmedia.h
api_name:
 - AM_QueryRate
product: Windows
targetos: Windows
req.typenames: AM_QueryRate
req.redist: 
---

# AM_QueryRate structure


## -description



The <b>AM_QueryRate</b> structure is used to query the decoder's maximum full-frame rate for forward and reverse playback.




## -struct-fields




### -field lMaxForwardFullFrame

Specifies the maximum forward full-frame rate, as rate x 10000.


### -field lMaxReverseFullFrame

Specifies the maximum reverse full-frame rate, as rate x 10000.


## -remarks



Rate is the inverse of speed. For example, if the playback speed is 2x, the rate is 1/2, so the <b>Rate</b> member is set to 5000. Reverse rates are negative.




## -see-also




<a href="https://msdn.microsoft.com/98808ed4-6d34-437b-9729-9cc805bc81f0">AM_RATE_QueryFullFrameRate Property</a>



<a href="https://msdn.microsoft.com/f88c64ce-af76-49fe-8ebd-029928506243">Rate Change Property Set</a>
 

 

