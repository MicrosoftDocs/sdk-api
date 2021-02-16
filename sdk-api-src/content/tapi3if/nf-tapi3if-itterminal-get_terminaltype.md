---
UID: NF:tapi3if.ITTerminal.get_TerminalType
title: ITTerminal::get_TerminalType (tapi3if.h)
description: The get_TerminalType method gets the TERMINAL_TYPE of the terminal.
helpviewer_keywords: ["ITTerminal interface [TAPI 2.2]","get_TerminalType method","ITTerminal.get_TerminalType","ITTerminal::get_TerminalType","_tapi3_itterminal_get_terminaltype","get_TerminalType","get_TerminalType method [TAPI 2.2]","get_TerminalType method [TAPI 2.2]","ITTerminal interface","tapi3.itterminal_get_terminaltype","tapi3if/ITTerminal::get_TerminalType"]
old-location: tapi3\itterminal_get_terminaltype.htm
tech.root: tapi3
ms.assetid: b6f33151-2415-4f24-b84b-7f2ce724db5b
ms.date: 12/05/2018
ms.keywords: ITTerminal interface [TAPI 2.2],get_TerminalType method, ITTerminal.get_TerminalType, ITTerminal::get_TerminalType, _tapi3_itterminal_get_terminaltype, get_TerminalType, get_TerminalType method [TAPI 2.2], get_TerminalType method [TAPI 2.2],ITTerminal interface, tapi3.itterminal_get_terminaltype, tapi3if/ITTerminal::get_TerminalType
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
 - ITTerminal::get_TerminalType
 - tapi3if/ITTerminal::get_TerminalType
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
 - ITTerminal.get_TerminalType
---

# ITTerminal::get_TerminalType


## -description

The 
<b>get_TerminalType</b> method gets the 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-terminal_type">TERMINAL_TYPE</a> of the terminal.

## -parameters

### -param pType [out]

Pointer to a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-terminal_type">TERMINAL_TYPE</a>.

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
The <i>pType</i> parameter is not a valid pointer.

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



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-terminal_type">TERMINAL_TYPE</a>



<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>



<a href="/windows/desktop/Tapi/terminal-object-interfaces">Terminal Object Interfaces</a>