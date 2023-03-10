---
UID: NF:tapi3if.ITTerminal.get_State
title: ITTerminal::get_State (tapi3if.h)
description: The get_State method gets the current state of the terminal.
helpviewer_keywords: ["ITTerminal interface [TAPI 2.2]","get_State method","ITTerminal.get_State","ITTerminal::get_State","_tapi3_itterminal_get_state","get_State","get_State method [TAPI 2.2]","get_State method [TAPI 2.2]","ITTerminal interface","tapi3.itterminal_get_state","tapi3if/ITTerminal::get_State"]
old-location: tapi3\itterminal_get_state.htm
tech.root: tapi3
ms.assetid: 18eebe2c-2c65-4836-a371-146eb76a379c
ms.date: 12/05/2018
ms.keywords: ITTerminal interface [TAPI 2.2],get_State method, ITTerminal.get_State, ITTerminal::get_State, _tapi3_itterminal_get_state, get_State, get_State method [TAPI 2.2], get_State method [TAPI 2.2],ITTerminal interface, tapi3.itterminal_get_state, tapi3if/ITTerminal::get_State
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
 - ITTerminal::get_State
 - tapi3if/ITTerminal::get_State
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
 - ITTerminal.get_State
---

# ITTerminal::get_State


## -description

The 
<b>get_State</b> method gets the current state of the terminal.

## -parameters

### -param pTerminalState [out]

Pointer to a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-terminal_state">TERMINAL_STATE</a> enum member.

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
The <i>pTerminalState</i> parameter is not a valid pointer.

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



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-terminal_state">TERMINAL_STATE</a>



<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>



<a href="/windows/desktop/Tapi/terminal-object-interfaces">Terminal Object Interfaces</a>