---
UID: NF:tapi3if.ITPrivateEvent.get_EventInterface
title: ITPrivateEvent::get_EventInterface (tapi3if.h)
description: The get_EventInterface method returns a pointer to the IDispatch interface of the private object's event handler.
helpviewer_keywords: ["ITPrivateEvent interface [TAPI 2.2]","get_EventInterface method","ITPrivateEvent.get_EventInterface","ITPrivateEvent::get_EventInterface","_tapi3_itprivateevent_get_eventinterface","get_EventInterface","get_EventInterface method [TAPI 2.2]","get_EventInterface method [TAPI 2.2]","ITPrivateEvent interface","tapi3.itprivateevent_get_eventinterface","tapi3if/ITPrivateEvent::get_EventInterface"]
old-location: tapi3\itprivateevent_get_eventinterface.htm
tech.root: tapi3
ms.assetid: c5620930-5cda-4f2e-8059-12af2d7f0a02
ms.date: 12/05/2018
ms.keywords: ITPrivateEvent interface [TAPI 2.2],get_EventInterface method, ITPrivateEvent.get_EventInterface, ITPrivateEvent::get_EventInterface, _tapi3_itprivateevent_get_eventinterface, get_EventInterface, get_EventInterface method [TAPI 2.2], get_EventInterface method [TAPI 2.2],ITPrivateEvent interface, tapi3.itprivateevent_get_eventinterface, tapi3if/ITPrivateEvent::get_EventInterface
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
 - ITPrivateEvent::get_EventInterface
 - tapi3if/ITPrivateEvent::get_EventInterface
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
 - ITPrivateEvent.get_EventInterface
---

# ITPrivateEvent::get_EventInterface


## -description

The 
<b>get_EventInterface</b> method returns a pointer to the <b>IDispatch</b> interface of the private object's event handler.

## -parameters

### -param pEventInterface [out]

 Pointer to the <b>IDispatch</b> interface of the private object's event handler.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
The <i>pEventInterface</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itprivateevent">ITPrivateEvent</a>