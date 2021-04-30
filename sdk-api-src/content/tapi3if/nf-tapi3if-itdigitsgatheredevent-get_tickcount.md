---
UID: NF:tapi3if.ITDigitsGatheredEvent.get_TickCount
title: ITDigitsGatheredEvent::get_TickCount (tapi3if.h)
description: The get_TickCount method gets the &quot;tick count&quot; (the number of milliseconds since Windows started) at which digit-gathering completed.
helpviewer_keywords: ["ITDigitsGatheredEvent interface [TAPI 2.2]","get_TickCount method","ITDigitsGatheredEvent.get_TickCount","ITDigitsGatheredEvent::get_TickCount","_tapi3_itdigitsgatheredevent_get_tickcount","get_TickCount","get_TickCount method [TAPI 2.2]","get_TickCount method [TAPI 2.2]","ITDigitsGatheredEvent interface","tapi3.itdigitsgatheredevent_get_tickcount","tapi3if/ITDigitsGatheredEvent::get_TickCount"]
old-location: tapi3\itdigitsgatheredevent_get_tickcount.htm
tech.root: tapi3
ms.assetid: 6e5fbed0-f132-418f-aa71-36d0e673affa
ms.date: 12/05/2018
ms.keywords: ITDigitsGatheredEvent interface [TAPI 2.2],get_TickCount method, ITDigitsGatheredEvent.get_TickCount, ITDigitsGatheredEvent::get_TickCount, _tapi3_itdigitsgatheredevent_get_tickcount, get_TickCount, get_TickCount method [TAPI 2.2], get_TickCount method [TAPI 2.2],ITDigitsGatheredEvent interface, tapi3.itdigitsgatheredevent_get_tickcount, tapi3if/ITDigitsGatheredEvent::get_TickCount
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
 - ITDigitsGatheredEvent::get_TickCount
 - tapi3if/ITDigitsGatheredEvent::get_TickCount
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
 - ITDigitsGatheredEvent.get_TickCount
---

# ITDigitsGatheredEvent::get_TickCount


## -description

The 
<b>get_TickCount</b> method gets the "tick count" (the number of milliseconds since Windows started) at which digit-gathering completed.

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

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itdigitsgatheredevent">ITDigitsGatheredEvent</a>