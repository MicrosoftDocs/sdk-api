---
UID: NF:tapi3if.ITAddressEvent.get_Terminal
title: ITAddressEvent::get_Terminal (tapi3if.h)
description: The get_Terminal method gets a pointer to the ITTerminal interface associated with the event.
helpviewer_keywords: ["ITAddressEvent interface [TAPI 2.2]","get_Terminal method","ITAddressEvent.get_Terminal","ITAddressEvent::get_Terminal","_tapi3_itaddressevent_get_terminal","get_Terminal","get_Terminal method [TAPI 2.2]","get_Terminal method [TAPI 2.2]","ITAddressEvent interface","tapi3.itaddressevent_get_terminal","tapi3if/ITAddressEvent::get_Terminal"]
old-location: tapi3\itaddressevent_get_terminal.htm
tech.root: tapi3
ms.assetid: a57a4eea-2a94-4c32-b98f-c1747c80fec3
ms.date: 12/05/2018
ms.keywords: ITAddressEvent interface [TAPI 2.2],get_Terminal method, ITAddressEvent.get_Terminal, ITAddressEvent::get_Terminal, _tapi3_itaddressevent_get_terminal, get_Terminal, get_Terminal method [TAPI 2.2], get_Terminal method [TAPI 2.2],ITAddressEvent interface, tapi3.itaddressevent_get_terminal, tapi3if/ITAddressEvent::get_Terminal
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
 - ITAddressEvent::get_Terminal
 - tapi3if/ITAddressEvent::get_Terminal
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
 - ITAddressEvent.get_Terminal
---

# ITAddressEvent::get_Terminal


## -description

The 
<b>get_Terminal</b> method gets a pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface associated with the event.

## -parameters

### -param ppTerminal [out]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface, or <b>NULL</b> if the event does not refer to a terminal.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppTerminal</i> parameter is not a valid pointer.

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
The <i>ppTerminal</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface returned by <b>ITAddressEvent::get_Terminal</b>. The application must call <b>Release</b> on the 
<b>ITTerminal</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent">ITAddressEvent</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>