---
UID: NF:tapi3cc.ITACDGroupEvent.get_Event
title: ITACDGroupEvent::get_Event (tapi3cc.h)
description: The ITACDGroupEvent::get_Event method (tapi3cc.h) gets the descriptor of an event which indicates that a new ACD group has been added.
helpviewer_keywords: ["ITACDGroupEvent interface [TAPI 2.2]","get_Event method","ITACDGroupEvent.get_Event","ITACDGroupEvent::get_Event","_tapi3_itacdgroupevent_get_event","get_Event","get_Event method [TAPI 2.2]","get_Event method [TAPI 2.2]","ITACDGroupEvent interface","tapi3.itacdgroupevent_get_event","tapi3cc/ITACDGroupEvent::get_Event"]
old-location: tapi3\itacdgroupevent_get_event.htm
tech.root: tapi3
ms.assetid: 9bc67911-cfb6-450c-bdc6-ade8d4617271
ms.date: 08/09/2022
ms.keywords: ITACDGroupEvent interface [TAPI 2.2],get_Event method, ITACDGroupEvent.get_Event, ITACDGroupEvent::get_Event, _tapi3_itacdgroupevent_get_event, get_Event, get_Event method [TAPI 2.2], get_Event method [TAPI 2.2],ITACDGroupEvent interface, tapi3.itacdgroupevent_get_event, tapi3cc/ITACDGroupEvent::get_Event
req.header: tapi3cc.h
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
 - ITACDGroupEvent::get_Event
 - tapi3cc/ITACDGroupEvent::get_Event
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
 - ITACDGroupEvent.get_Event
---

# ITACDGroupEvent::get_Event


## -description

The 
<b>get_Event</b> method gets the descriptor of an event which indicates that a new ACD group has been added.

## -parameters

### -param pEvent [out]

Pointer to 
<a href="/windows/desktop/api/tapi3/ne-tapi3-acdgroup_event">ACDGROUP_EVENT</a> descriptor of event.

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
The <i>pEvent</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

The ACDGE_NEW_GROUP and ACDGE_REMOVE_GROUP values are not currently supported.

## -see-also

<a href="/windows/desktop/api/tapi3/ne-tapi3-acdgroup_event">ACDGROUP_EVENT</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itacdgroupevent">ITACDGroupEvent</a>
