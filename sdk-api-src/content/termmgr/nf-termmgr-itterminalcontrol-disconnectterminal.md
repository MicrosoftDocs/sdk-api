---
UID: NF:termmgr.ITTerminalControl.DisconnectTerminal
title: ITTerminalControl::DisconnectTerminal
author: windows-sdk-content
description: The DisconnectTerminal method disconnects internal filters and removes them from the filter graph.
old-location: tapi3\itterminalcontrol_disconnectterminal.htm
old-project: Tapi
ms.assetid: 5af5d0bf-27e1-4d42-a003-79388d2498cd
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: DisconnectTerminal, DisconnectTerminal method [TAPI 2.2], DisconnectTerminal method [TAPI 2.2],ITTerminalControl interface, ITTerminalControl interface [TAPI 2.2],DisconnectTerminal method, ITTerminalControl.DisconnectTerminal, ITTerminalControl::DisconnectTerminal, _tapi3_itterminalcontrol_disconnectterminal, tapi3.itterminalcontrol_disconnectterminal, termmgr/ITTerminalControl::DisconnectTerminal
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TMGR_DIRECTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Termmgr.h
api_name:
 - ITTerminalControl.DisconnectTerminal
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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




<a href="https://msdn.microsoft.com/6fe60002-3af3-45e9-a084-7296a48e7263">ITTerminalControl</a>
 

 

