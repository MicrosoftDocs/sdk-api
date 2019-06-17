---
UID: NN:termmgr.ITTerminalControl
title: ITTerminalControl (termmgr.h)
author: windows-sdk-content
description: The ITTerminalControl interface provides methods to get the MSP handle, connect and disconnect a terminal from a filter graph, and run or stop a renderer.
old-location: tapi3\itterminalcontrol.htm
tech.root: Tapi
ms.assetid: 6fe60002-3af3-45e9-a084-7296a48e7263
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITTerminalControl, ITTerminalControl interface [TAPI 2.2], ITTerminalControl interface [TAPI 2.2],described, _tapi3_itterminalcontrol, tapi3.itterminalcontrol, termmgr/ITTerminalControl
ms.topic: interface
f1_keywords: ["termmgr/ITTerminalControl"]
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
 - ITTerminalControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITTerminalControl interface


## -description


The 
<b>ITTerminalControl</b> interface provides methods to get the MSP handle, connect and disconnect a terminal from a filter graph, and run or stop a renderer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITTerminalControl</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITTerminalControl</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itterminalcontrol-completeconnectterminal">CompleteConnectTerminal</a>
</td>
<td align="left" width="63%">
Completes terminal connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itterminalcontrol-connectterminal">ConnectTerminal</a>
</td>
<td align="left" width="63%">
Connects filters and returns a set of pins for connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itterminalcontrol-disconnectterminal">DisconnectTerminal</a>
</td>
<td align="left" width="63%">
Disconnects internal filters and removes them from the filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itterminalcontrol-get_addresshandle">get_AddressHandle</a>
</td>
<td align="left" width="63%">
Gets MSP address handle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itterminalcontrol-runrenderfilter">RunRenderFilter</a>
</td>
<td align="left" width="63%">
Starts the rightmost render filter in the terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itterminalcontrol-stoprenderfilter">StopRenderFilter</a>
</td>
<td align="left" width="63%">
Stops the rightmost render filter in the terminal.

</td>
</tr>
</table> 

