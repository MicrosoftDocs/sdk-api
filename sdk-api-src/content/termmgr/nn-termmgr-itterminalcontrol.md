---
UID: NN:termmgr.ITTerminalControl
title: ITTerminalControl
author: windows-sdk-content
description: The ITTerminalControl interface provides methods to get the MSP handle, connect and disconnect a terminal from a filter graph, and run or stop a renderer.
old-location: tapi3\itterminalcontrol.htm
old-project: Tapi
ms.assetid: 6fe60002-3af3-45e9-a084-7296a48e7263
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITTerminalControl, ITTerminalControl interface [TAPI 2.2], ITTerminalControl interface [TAPI 2.2],described, _tapi3_itterminalcontrol, tapi3.itterminalcontrol, termmgr/ITTerminalControl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.typenames: TMGR_DIRECTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Termmgr.h
api_name:
-	ITTerminalControl
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITTerminalControl interface


## -description


The 
<b>ITTerminalControl</b> interface provides methods to get the MSP handle, connect and disconnect a terminal from a filter graph, and run or stop a renderer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITTerminalControl</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITTerminalControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITTerminalControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f40b0c1-2c5e-4520-9406-6bebb3da65d0">CompleteConnectTerminal</a>
</td>
<td align="left" width="63%">
Completes terminal connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0351e645-b857-44d8-a226-046ebe0f4c81">ConnectTerminal</a>
</td>
<td align="left" width="63%">
Connects filters and returns a set of pins for connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5af5d0bf-27e1-4d42-a003-79388d2498cd">DisconnectTerminal</a>
</td>
<td align="left" width="63%">
Disconnects internal filters and removes them from the filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f222dea-059a-4eda-bcbc-cd6c61cdf2fa">get_AddressHandle</a>
</td>
<td align="left" width="63%">
Gets MSP address handle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed02ed04-3665-47be-a77b-7804a2197767">RunRenderFilter</a>
</td>
<td align="left" width="63%">
Starts the rightmost render filter in the terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30a47de7-c54d-4600-9b4b-07013f962c4d">StopRenderFilter</a>
</td>
<td align="left" width="63%">
Stops the rightmost render filter in the terminal.

</td>
</tr>
</table> 

