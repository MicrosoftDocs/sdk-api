---
UID: NF:tapi3if.ITTerminal.get_TerminalClass
title: ITTerminal::get_TerminalClass (tapi3if.h)
description: The get_TerminalClass method gets the Terminal Class of the terminal.
helpviewer_keywords: ["ITTerminal interface [TAPI 2.2]","get_TerminalClass method","ITTerminal.get_TerminalClass","ITTerminal::get_TerminalClass","_tapi3_itterminal_get_terminalclass","get_TerminalClass","get_TerminalClass method [TAPI 2.2]","get_TerminalClass method [TAPI 2.2]","ITTerminal interface","tapi3.itterminal_get_terminalclass","tapi3if/ITTerminal::get_TerminalClass"]
old-location: tapi3\itterminal_get_terminalclass.htm
tech.root: tapi3
ms.assetid: a31543da-4cb8-4719-8e33-fcb4d9d630b1
ms.date: 12/05/2018
ms.keywords: ITTerminal interface [TAPI 2.2],get_TerminalClass method, ITTerminal.get_TerminalClass, ITTerminal::get_TerminalClass, _tapi3_itterminal_get_terminalclass, get_TerminalClass, get_TerminalClass method [TAPI 2.2], get_TerminalClass method [TAPI 2.2],ITTerminal interface, tapi3.itterminal_get_terminalclass, tapi3if/ITTerminal::get_TerminalClass
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
 - ITTerminal::get_TerminalClass
 - tapi3if/ITTerminal::get_TerminalClass
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
 - ITTerminal.get_TerminalClass
---

# ITTerminal::get_TerminalClass


## -description

The 
<b>get_TerminalClass</b> method gets the 
<a href="/windows/desktop/Tapi/terminal-class">Terminal Class</a> of the terminal.

## -parameters

### -param ppTerminalClass [out]

Pointer to <b>BSTR</b> representation of the 
<a href="/windows/desktop/Tapi/terminal-class">Terminal Class</a> of the terminal.

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
The <i>ppTerminalClass</i> parameter is not a valid pointer.

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

## -remarks

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory allocated for the <i>ppTerminalClass</i> parameter.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>



<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>



<a href="/windows/desktop/Tapi/terminal-object-interfaces">Terminal Object Interfaces</a>