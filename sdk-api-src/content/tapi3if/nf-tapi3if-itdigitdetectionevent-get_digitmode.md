---
UID: NF:tapi3if.ITDigitDetectionEvent.get_DigitMode
title: ITDigitDetectionEvent::get_DigitMode (tapi3if.h)
description: The get_DigitMode method gets the indicator of the line digit mode, such as LINEDIGITMODE_DTMF.
helpviewer_keywords: ["ITDigitDetectionEvent interface [TAPI 2.2]","get_DigitMode method","ITDigitDetectionEvent.get_DigitMode","ITDigitDetectionEvent::get_DigitMode","_tapi3_itdigitdetectionevent_get_digitmode","get_DigitMode","get_DigitMode method [TAPI 2.2]","get_DigitMode method [TAPI 2.2]","ITDigitDetectionEvent interface","tapi3.itdigitdetectionevent_get_digitmode","tapi3if/ITDigitDetectionEvent::get_DigitMode"]
old-location: tapi3\itdigitdetectionevent_get_digitmode.htm
tech.root: tapi3
ms.assetid: 7eeda641-9155-4628-b4b2-2d427a255d7c
ms.date: 12/05/2018
ms.keywords: ITDigitDetectionEvent interface [TAPI 2.2],get_DigitMode method, ITDigitDetectionEvent.get_DigitMode, ITDigitDetectionEvent::get_DigitMode, _tapi3_itdigitdetectionevent_get_digitmode, get_DigitMode, get_DigitMode method [TAPI 2.2], get_DigitMode method [TAPI 2.2],ITDigitDetectionEvent interface, tapi3.itdigitdetectionevent_get_digitmode, tapi3if/ITDigitDetectionEvent::get_DigitMode
req.header: tapi3if.h
req.include-header: Tapi3.h
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
 - ITDigitDetectionEvent::get_DigitMode
 - tapi3if/ITDigitDetectionEvent::get_DigitMode
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
 - ITDigitDetectionEvent.get_DigitMode
---

# ITDigitDetectionEvent::get_DigitMode


## -description

The 
<b>get_DigitMode</b> method gets the indicator of the 
<a href="/windows/desktop/Tapi/linedigitmode--constants">line digit mode</a>, such as LINEDIGITMODE_DTMF.

## -parameters

### -param pDigitMode [out]

Pointer to indicator of digit mode.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pDigitMode</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itdigitdetectionevent">ITDigitDetectionEvent</a>