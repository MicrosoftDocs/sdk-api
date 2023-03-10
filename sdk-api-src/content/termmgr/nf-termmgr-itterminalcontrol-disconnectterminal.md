---
UID: NF:termmgr.ITTerminalControl.DisconnectTerminal
title: ITTerminalControl::DisconnectTerminal (termmgr.h)
description: The DisconnectTerminal method disconnects internal filters and removes them from the filter graph.
helpviewer_keywords: ["DisconnectTerminal","DisconnectTerminal method [TAPI 2.2]","DisconnectTerminal method [TAPI 2.2]","ITTerminalControl interface","ITTerminalControl interface [TAPI 2.2]","DisconnectTerminal method","ITTerminalControl.DisconnectTerminal","ITTerminalControl::DisconnectTerminal","_tapi3_itterminalcontrol_disconnectterminal","tapi3.itterminalcontrol_disconnectterminal","termmgr/ITTerminalControl::DisconnectTerminal"]
old-location: tapi3\itterminalcontrol_disconnectterminal.htm
tech.root: tapi3
ms.assetid: 5af5d0bf-27e1-4d42-a003-79388d2498cd
ms.date: 12/05/2018
ms.keywords: DisconnectTerminal, DisconnectTerminal method [TAPI 2.2], DisconnectTerminal method [TAPI 2.2],ITTerminalControl interface, ITTerminalControl interface [TAPI 2.2],DisconnectTerminal method, ITTerminalControl.DisconnectTerminal, ITTerminalControl::DisconnectTerminal, _tapi3_itterminalcontrol_disconnectterminal, tapi3.itterminalcontrol_disconnectterminal, termmgr/ITTerminalControl::DisconnectTerminal
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
 - ITTerminalControl::DisconnectTerminal
 - termmgr/ITTerminalControl::DisconnectTerminal
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
 - ITTerminalControl.DisconnectTerminal
---

# ITTerminalControl::DisconnectTerminal


## -description

The 
<b>DisconnectTerminal</b> method disconnects internal filters and removes them from the filter graph.

## -parameters

### -param pGraph [in]

Pointer to the interface for the graph to be disconnected.

### -param dwReserved [in]

Reserved; not currently used.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unknown error occurred during the disconnect attempt.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/termmgr/nn-termmgr-itterminalcontrol">ITTerminalControl</a>