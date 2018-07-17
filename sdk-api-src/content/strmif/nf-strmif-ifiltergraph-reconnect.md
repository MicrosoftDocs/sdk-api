---
UID: NF:strmif.IFilterGraph.Reconnect
title: IFilterGraph::Reconnect
author: windows-sdk-content
description: The Reconnect method disconnects a pin and then reconnects it to the same pin.
old-location: dshow\ifiltergraph_reconnect.htm
old-project: DirectShow
ms.assetid: 98a46014-031b-4f35-b1bc-58aef411360b
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IFilterGraph interface [DirectShow],Reconnect method, IFilterGraph.Reconnect, IFilterGraph::Reconnect, IFilterGraphReconnect, Reconnect, Reconnect method [DirectShow], Reconnect method [DirectShow],IFilterGraph interface, dshow.ifiltergraph_reconnect, strmif/IFilterGraph::Reconnect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IFilterGraph.Reconnect
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IFilterGraph::Reconnect


## -description



The <code>Reconnect</code> method disconnects a pin and then reconnects it to the same pin.



Applications should not call this method. It is called by filters during the graph building process.


## -parameters




### -param ppin [in]

Pointer to <a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin</a> interface of the pin to reconnect.


## -returns



Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
Pin is not connected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
Filter is not stopped.

</td>
</tr>
</table>
 




## -remarks



This method is obsolete; use the <a href="https://msdn.microsoft.com/a72cf427-056b-4751-9c4a-665251e549f8">IFilterGraph2::ReconnectEx</a> method instead.

Filters can call this method in order to renegotiate a pin connection. The method executes on a separate thread. Before calling this method, call <a href="https://msdn.microsoft.com/ed11eeef-464b-4a75-958b-2bc6dbc7af04">IPin::QueryAccept</a> on the other pin to ensure that the reconnnection attempt will succeed. Do not call this method unless <b>QueryAccept</b> returns S_OK. Otherwise, because the reconnection is performed asynchronously, the reconnection might fail even though the <code>Reconnect</code> method succeeds, leaving the filter graph in an inconsistent state.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/73a92f44-03c6-47e3-98d1-a20100ed8fa1">IFilterGraph Interface</a>



<a href="https://msdn.microsoft.com/34b3e4de-e4eb-48c5-aaef-fc99b63e8691">Reconnecting Pins</a>
 

 

