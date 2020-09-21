---
UID: NF:tapi3if.ITToneDetectionEvent.get_TickCount
title: ITToneDetectionEvent::get_TickCount (tapi3if.h)
description: The get_TickCount method gets the &quot;tick count&quot; (the number of milliseconds since Windows started) at which the tone was detected.
helpviewer_keywords: ["ITToneDetectionEvent interface [TAPI 2.2]","get_TickCount method","ITToneDetectionEvent.get_TickCount","ITToneDetectionEvent::get_TickCount","_tapi3_ittonedetectionevent_get_tickcount","get_TickCount","get_TickCount method [TAPI 2.2]","get_TickCount method [TAPI 2.2]","ITToneDetectionEvent interface","tapi3.ittonedetectionevent_get_tickcount","tapi3if/ITToneDetectionEvent::get_TickCount"]
old-location: tapi3\ittonedetectionevent_get_tickcount.htm
tech.root: tapi3
ms.assetid: 01a00b2c-d4b0-4de0-91b8-0741ed1fd300
ms.date: 12/05/2018
ms.keywords: ITToneDetectionEvent interface [TAPI 2.2],get_TickCount method, ITToneDetectionEvent.get_TickCount, ITToneDetectionEvent::get_TickCount, _tapi3_ittonedetectionevent_get_tickcount, get_TickCount, get_TickCount method [TAPI 2.2], get_TickCount method [TAPI 2.2],ITToneDetectionEvent interface, tapi3.ittonedetectionevent_get_tickcount, tapi3if/ITToneDetectionEvent::get_TickCount
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
 - ITToneDetectionEvent::get_TickCount
 - tapi3if/ITToneDetectionEvent::get_TickCount
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
 - ITToneDetectionEvent.get_TickCount
---

# ITToneDetectionEvent::get_TickCount


## -description

The 
<b>get_TickCount</b> method gets the "tick count" (the number of milliseconds since Windows started) at which the tone was detected.

## -parameters

### -param plTickCount [out]

Pointer to a value to receive the tick count.

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
The <i>plTickCount</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittonedetectionevent">ITToneDetectionEvent</a>