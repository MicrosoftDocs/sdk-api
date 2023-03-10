---
UID: NF:termmgr.ITTerminalControl.CompleteConnectTerminal
title: ITTerminalControl::CompleteConnectTerminal (termmgr.h)
description: The CompleteConnectTerminal method completes the terminal connection.
helpviewer_keywords: ["CompleteConnectTerminal","CompleteConnectTerminal method [TAPI 2.2]","CompleteConnectTerminal method [TAPI 2.2]","ITTerminalControl interface","ITTerminalControl interface [TAPI 2.2]","CompleteConnectTerminal method","ITTerminalControl.CompleteConnectTerminal","ITTerminalControl::CompleteConnectTerminal","_tapi3_itterminalcontrol_completeconnectterminal","tapi3.itterminalcontrol_completeconnectterminal","termmgr/ITTerminalControl::CompleteConnectTerminal"]
old-location: tapi3\itterminalcontrol_completeconnectterminal.htm
tech.root: tapi3
ms.assetid: 1f40b0c1-2c5e-4520-9406-6bebb3da65d0
ms.date: 12/05/2018
ms.keywords: CompleteConnectTerminal, CompleteConnectTerminal method [TAPI 2.2], CompleteConnectTerminal method [TAPI 2.2],ITTerminalControl interface, ITTerminalControl interface [TAPI 2.2],CompleteConnectTerminal method, ITTerminalControl.CompleteConnectTerminal, ITTerminalControl::CompleteConnectTerminal, _tapi3_itterminalcontrol_completeconnectterminal, tapi3.itterminalcontrol_completeconnectterminal, termmgr/ITTerminalControl::CompleteConnectTerminal
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
 - ITTerminalControl::CompleteConnectTerminal
 - termmgr/ITTerminalControl::CompleteConnectTerminal
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
 - ITTerminalControl.CompleteConnectTerminal
---

# ITTerminalControl::CompleteConnectTerminal


## -description

The 
<b>CompleteConnectTerminal</b> method completes the terminal connection.



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
</table>

## -remarks

This method always returns S_OK. If an MSP cannot connect the terminal, the error return must occur during the call to 
<a href="/windows/desktop/api/termmgr/nf-termmgr-itterminalcontrol-connectterminal">ITTerminalControl::ConnectTerminal</a>.

## -see-also

<a href="/windows/desktop/api/termmgr/nn-termmgr-itterminalcontrol">ITTerminalControl</a>
