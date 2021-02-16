---
UID: NF:termmgr.ITTerminalControl.ConnectTerminal
title: ITTerminalControl::ConnectTerminal (termmgr.h)
description: The ConnectTerminal method connects filters and returns a set of pins for connection. Enters each of the internal filters into the filter graph, connects the internal filters together (if applicable) and returns a set of pins for connection.
helpviewer_keywords: ["ConnectTerminal","ConnectTerminal method [TAPI 2.2]","ConnectTerminal method [TAPI 2.2]","ITTerminalControl interface","ITTerminalControl interface [TAPI 2.2]","ConnectTerminal method","ITTerminalControl.ConnectTerminal","ITTerminalControl::ConnectTerminal","_tapi3_itterminalcontrol_connectterminal","tapi3.itterminalcontrol_connectterminal","termmgr/ITTerminalControl::ConnectTerminal"]
old-location: tapi3\itterminalcontrol_connectterminal.htm
tech.root: tapi3
ms.assetid: 0351e645-b857-44d8-a226-046ebe0f4c81
ms.date: 12/05/2018
ms.keywords: ConnectTerminal, ConnectTerminal method [TAPI 2.2], ConnectTerminal method [TAPI 2.2],ITTerminalControl interface, ITTerminalControl interface [TAPI 2.2],ConnectTerminal method, ITTerminalControl.ConnectTerminal, ITTerminalControl::ConnectTerminal, _tapi3_itterminalcontrol_connectterminal, tapi3.itterminalcontrol_connectterminal, termmgr/ITTerminalControl::ConnectTerminal
req.header: termmgr.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITTerminalControl::ConnectTerminal
 - termmgr/ITTerminalControl::ConnectTerminal
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Termmgr.h
api_name:
 - ITTerminalControl.ConnectTerminal
---

# ITTerminalControl::ConnectTerminal


## -description

The 
<b>ConnectTerminal</b> method connects filters and returns a set of pins for connection. Enters each of the internal filters into the filter graph, connects the internal filters together (if applicable) and returns a set of pins for connection.

## -parameters

### -param pGraph [in]

Pointer to graph builder interface.

### -param dwTerminalDirection [in]

Indicator of 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-terminal_direction">terminal direction</a>.

### -param pdwNumPins [in, out]

Pointer to number of pins.

### -param ppPins [out]

Pointer to array of pins to be used for media transport related to the current terminal.

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
<dt><b>TAPI_E_NOTENOUGHMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_TERMINALINUSE</b></dt>
</dl>
</td>
<td width="60%">
The current terminal is already in use.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/termmgr/nn-termmgr-itterminalcontrol">ITTerminalControl</a>