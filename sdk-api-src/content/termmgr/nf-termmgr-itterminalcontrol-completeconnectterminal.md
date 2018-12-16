---
UID: NF:termmgr.ITTerminalControl.CompleteConnectTerminal
title: ITTerminalControl::CompleteConnectTerminal
author: windows-sdk-content
description: The CompleteConnectTerminal method completes the terminal connection.
old-location: tapi3\itterminalcontrol_completeconnectterminal.htm
tech.root: tapi
ms.assetid: 1f40b0c1-2c5e-4520-9406-6bebb3da65d0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CompleteConnectTerminal, CompleteConnectTerminal method [TAPI 2.2], CompleteConnectTerminal method [TAPI 2.2],ITTerminalControl interface, ITTerminalControl interface [TAPI 2.2],CompleteConnectTerminal method, ITTerminalControl.CompleteConnectTerminal, ITTerminalControl::CompleteConnectTerminal, _tapi3_itterminalcontrol_completeconnectterminal, tapi3.itterminalcontrol_completeconnectterminal, termmgr/ITTerminalControl::CompleteConnectTerminal
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Termmgr.h
api_name:
 - ITTerminalControl.CompleteConnectTerminal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITTerminalControl::CompleteConnectTerminal


## -description


The 
<b>CompleteConnectTerminal</b> method completes the terminal connection.


## -parameters






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
<a href="https://msdn.microsoft.com/0351e645-b857-44d8-a226-046ebe0f4c81">ITTerminalControl::ConnectTerminal</a>.




## -see-also




<a href="https://msdn.microsoft.com/6fe60002-3af3-45e9-a084-7296a48e7263">ITTerminalControl</a>
 

 

