---
UID: NF:tapi3if.ITTerminal.get_Direction
title: ITTerminal::get_Direction (tapi3if.h)
description: The get_Direction method gets a TERMINAL_DIRECTION descriptor of the media stream direction for the terminal.
helpviewer_keywords: ["ITTerminal interface [TAPI 2.2]","get_Direction method","ITTerminal.get_Direction","ITTerminal::get_Direction","_tapi3_itterminal_get_direction","get_Direction","get_Direction method [TAPI 2.2]","get_Direction method [TAPI 2.2]","ITTerminal interface","tapi3.itterminal_get_direction","tapi3if/ITTerminal::get_Direction"]
old-location: tapi3\itterminal_get_direction.htm
tech.root: tapi3
ms.assetid: e0a69c3d-1780-4088-8249-961788dbf184
ms.date: 12/05/2018
ms.keywords: ITTerminal interface [TAPI 2.2],get_Direction method, ITTerminal.get_Direction, ITTerminal::get_Direction, _tapi3_itterminal_get_direction, get_Direction, get_Direction method [TAPI 2.2], get_Direction method [TAPI 2.2],ITTerminal interface, tapi3.itterminal_get_direction, tapi3if/ITTerminal::get_Direction
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITTerminal::get_Direction
 - tapi3if/ITTerminal::get_Direction
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tapi3if.h
api_name:
 - ITTerminal.get_Direction
---

# ITTerminal::get_Direction


## -description

The 
<b>get_Direction</b> method gets a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-terminal_direction">TERMINAL_DIRECTION</a> descriptor of the media stream direction for the terminal.

## -parameters

### -param pDirection [out]

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-terminal_direction">TERMINAL_DIRECTION</a> descriptor of the media stream direction for the terminal.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pDirection</i> parameter is not a valid pointer.

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
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-terminal_direction">TERMINAL_DIRECTION</a>



<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>



<a href="/windows/desktop/Tapi/terminal-object-interfaces">Terminal Object Interfaces</a>