---
UID: NF:tapi3if.ITDetectTone.get_Duration
title: ITDetectTone::get_Duration (tapi3if.h)
description: The get_Duration method retrieves the length of time during which a tone should be present before the TAPI Server generates a tone event.
helpviewer_keywords: ["ITDetectTone interface [TAPI 2.2]","get_Duration method","ITDetectTone.get_Duration","ITDetectTone::get_Duration","_tapi3_itdetecttone_get_duration","get_Duration","get_Duration method [TAPI 2.2]","get_Duration method [TAPI 2.2]","ITDetectTone interface","tapi3.itdetecttone_get_duration","tapi3if/ITDetectTone::get_Duration"]
old-location: tapi3\itdetecttone_get_duration.htm
tech.root: tapi3
ms.assetid: 3c1f8900-1384-4fb5-8931-90bb0d100d41
ms.date: 12/05/2018
ms.keywords: ITDetectTone interface [TAPI 2.2],get_Duration method, ITDetectTone.get_Duration, ITDetectTone::get_Duration, _tapi3_itdetecttone_get_duration, get_Duration, get_Duration method [TAPI 2.2], get_Duration method [TAPI 2.2],ITDetectTone interface, tapi3.itdetecttone_get_duration, tapi3if/ITDetectTone::get_Duration
req.header: tapi3if.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITDetectTone::get_Duration
 - tapi3if/ITDetectTone::get_Duration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITDetectTone.get_Duration
---

# ITDetectTone::get_Duration


## -description

The 
<b>get_Duration</b> method retrieves the length of time during which a tone should be present before the TAPI Server generates a tone event.

## -parameters

### -param plDuration [out]

Pointer to a value that receives the tone duration, in milliseconds, during which the specified tone should be present.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>plDuration</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itdetecttone">ITDetectTone</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itdetecttone-put_duration">put_Duration</a>