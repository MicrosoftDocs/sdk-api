---
UID: NS:dvdmedia.AM_QueryRate
title: AM_QueryRate (dvdmedia.h)
description: The AM_QueryRate structure is used to query the decoder's maximum full-frame rate for forward and reverse playback.
helpviewer_keywords: ["AM_QueryRate","AM_QueryRate structure [DirectShow]","AM_QueryRateStructure","dshow.am_queryrate","dvdmedia/AM_QueryRate"]
old-location: dshow\am_queryrate.htm
tech.root: dshow
ms.assetid: a791f6ac-f415-4641-bac1-26db983a1ef7
ms.date: 12/05/2018
ms.keywords: AM_QueryRate, AM_QueryRate structure [DirectShow], AM_QueryRateStructure, dshow.am_queryrate, dvdmedia/AM_QueryRate
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
targetos: Windows
req.typenames: AM_QueryRate
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AM_QueryRate
 - dvdmedia/AM_QueryRate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dvdmedia.h
api_name:
 - AM_QueryRate
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

<a href="/windows/desktop/DirectShow/am-rate-queryfullframerate-property">AM_RATE_QueryFullFrameRate Property</a>



<a href="/windows/desktop/DirectShow/rate-change-property-set">Rate Change Property Set</a>

