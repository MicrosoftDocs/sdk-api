---
UID: NF:tapi3if.ITDigitDetectionEvent.get_TickCount
title: ITDigitDetectionEvent::get_TickCount (tapi3if.h)
description: The get_TickCount method gets the &quot;tick count&quot; (number of milliseconds since Windows started) at which the digit gathering completed.
helpviewer_keywords: ["ITDigitDetectionEvent interface [TAPI 2.2]","get_TickCount method","ITDigitDetectionEvent.get_TickCount","ITDigitDetectionEvent::get_TickCount","_tapi3_itdigitdetectionevent_get_tickcount","get_TickCount","get_TickCount method [TAPI 2.2]","get_TickCount method [TAPI 2.2]","ITDigitDetectionEvent interface","tapi3.itdigitdetectionevent_get_tickcount","tapi3if/ITDigitDetectionEvent::get_TickCount"]
old-location: tapi3\itdigitdetectionevent_get_tickcount.htm
tech.root: tapi3
ms.assetid: 24c83763-366b-4e1b-8662-9d87250b7945
ms.date: 12/05/2018
ms.keywords: ITDigitDetectionEvent interface [TAPI 2.2],get_TickCount method, ITDigitDetectionEvent.get_TickCount, ITDigitDetectionEvent::get_TickCount, _tapi3_itdigitdetectionevent_get_tickcount, get_TickCount, get_TickCount method [TAPI 2.2], get_TickCount method [TAPI 2.2],ITDigitDetectionEvent interface, tapi3.itdigitdetectionevent_get_tickcount, tapi3if/ITDigitDetectionEvent::get_TickCount
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
 - ITDigitDetectionEvent::get_TickCount
 - tapi3if/ITDigitDetectionEvent::get_TickCount
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
 - ITDigitDetectionEvent.get_TickCount
---

# ITDigitDetectionEvent::get_TickCount


## -description

The 
<b>get_TickCount</b> method gets the "tick count" (number of milliseconds since Windows started) at which the digit gathering completed.

## -parameters

### -param plTickCount [out]

Pointer to tick count.

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
The <i>plTickCount</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itdigitdetectionevent">ITDigitDetectionEvent</a>