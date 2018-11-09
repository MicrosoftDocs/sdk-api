---
UID: NF:strmif.IFilterGraph2.ReconnectEx
title: IFilterGraph2::ReconnectEx
author: windows-sdk-content
description: The ReconnectEx method breaks the existing pin connection and reconnects it to the same pin, using a specified media type.
old-location: dshow\ifiltergraph2_reconnectex.htm
tech.root: DirectShow
ms.assetid: a72cf427-056b-4751-9c4a-665251e549f8
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IFilterGraph2 interface [DirectShow],ReconnectEx method, IFilterGraph2.ReconnectEx, IFilterGraph2::ReconnectEx, IFilterGraph2ReconnectEx, ReconnectEx, ReconnectEx method [DirectShow], ReconnectEx method [DirectShow],IFilterGraph2 interface, dshow.ifiltergraph2_reconnectex, strmif/IFilterGraph2::ReconnectEx
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IFilterGraph2.ReconnectEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFilterGraph2::ReconnectEx


## -description



The <code>ReconnectEx</code> method breaks the existing pin connection and reconnects it to the same pin, using a specified media type.



Applications should not call this method. It is called by filters during the graph building process.


## -parameters




### -param ppin [in]

Pointer to the pin to disconnect and reconnect.


### -param pmt [in]

Pointer to the media type to reconnect with. Specify <b>NULL</b> to use the existing media type.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Pin was not connected. No error.

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
<dt><b>VFW_E_NOT_STOPPED</b></dt>
</dl>
</td>
<td width="60%">
The filter is not stopped, but it does not support reconnection while in a running state.

</td>
</tr>
</table>
 




## -remarks



Filters can call this method in order to renegotiate a pin connection. The method executes on a separate thread. Before calling this method, call <a href="https://msdn.microsoft.com/ed11eeef-464b-4a75-958b-2bc6dbc7af04">IPin::QueryAccept</a> on the other pin to ensure that the reconnnection attempt will succeed. Do not call this method unless <b>QueryAccept</b> returns S_OK. Otherwise, because the reconnection is performed asynchronously, the reconnection might fail even though the <code>ReconnectEx</code> method succeeds, leaving the filter graph in an inconsistent state.

This method improves on the <a href="https://msdn.microsoft.com/98a46014-031b-4f35-b1bc-58aef411360b">IFilterGraph::Reconnect</a> method by specifying a media type. This makes the reconnection more likely to succeed.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/1a1ef4fe-a054-4ba7-99c7-1f209472c5a6">IFilterGraph2 Interface</a>



<a href="https://msdn.microsoft.com/34b3e4de-e4eb-48c5-aaef-fc99b63e8691">Reconnecting Pins</a>
 

 

