---
UID: NS:dvdmedia.__unnamed_struct_7
title: AM_QueryRate (dvdmedia.h)
author: windows-sdk-content
description: The AM_QueryRate structure is used to query the decoder's maximum full-frame rate for forward and reverse playback.
old-location: dshow\am_queryrate.htm
tech.root: DirectShow
ms.assetid: a791f6ac-f415-4641-bac1-26db983a1ef7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AM_QueryRate, AM_QueryRate structure [DirectShow], AM_QueryRateStructure, dshow.am_queryrate, dvdmedia/AM_QueryRate
ms.topic: struct
f1_keywords: 
 - "dvdmedia/AM_QueryRate"
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
targetos: Windows
req.typenames: AM_QueryRate
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/am-rate-queryfullframerate-property">AM_RATE_QueryFullFrameRate Property</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/rate-change-property-set">Rate Change Property Set</a>
 

 

