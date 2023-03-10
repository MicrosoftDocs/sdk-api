---
UID: NF:tapi3if.ITDetectTone.put_Duration
title: ITDetectTone::put_Duration (tapi3if.h)
description: The put_Duration method sets the length of time during which a tone should be present before the TAPI Server generates a tone event.
helpviewer_keywords: ["ITDetectTone interface [TAPI 2.2]","put_Duration method","ITDetectTone.put_Duration","ITDetectTone::put_Duration","_tapi3_itdetecttone_put_duration","put_Duration","put_Duration method [TAPI 2.2]","put_Duration method [TAPI 2.2]","ITDetectTone interface","tapi3.itdetecttone_put_duration","tapi3if/ITDetectTone::put_Duration"]
old-location: tapi3\itdetecttone_put_duration.htm
tech.root: tapi3
ms.assetid: a64181ca-e8d6-48fc-89ef-b91268b709aa
ms.date: 12/05/2018
ms.keywords: ITDetectTone interface [TAPI 2.2],put_Duration method, ITDetectTone.put_Duration, ITDetectTone::put_Duration, _tapi3_itdetecttone_put_duration, put_Duration, put_Duration method [TAPI 2.2], put_Duration method [TAPI 2.2],ITDetectTone interface, tapi3.itdetecttone_put_duration, tapi3if/ITDetectTone::put_Duration
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
 - ITDetectTone::put_Duration
 - tapi3if/ITDetectTone::put_Duration
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
 - ITDetectTone.put_Duration
---

# ITDetectTone::put_Duration


## -description

The 
<b>put_Duration</b> method sets the length of time during which a tone should be present before the TAPI Server generates a tone event.

## -parameters

### -param lDuration [in]

Specifies the tone duration, in milliseconds, during which the specified tone should be present.

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
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itdetecttone">ITDetectTone</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itdetecttone-get_duration">get_Duration</a>