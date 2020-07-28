---
UID: NF:strmif.IFilterGraph.Disconnect
title: IFilterGraph::Disconnect (strmif.h)
description: The Disconnect method disconnects this pin.
helpviewer_keywords: ["Disconnect","Disconnect method [DirectShow]","Disconnect method [DirectShow]","IFilterGraph interface","Disconnect method [DirectShow]","IGraphBuilder interface","IFilterGraph interface [DirectShow]","Disconnect method","IFilterGraph.Disconnect","IFilterGraph::Disconnect","IFilterGraphDisconnect","IGraphBuilder interface [DirectShow]","Disconnect method","IGraphBuilder.Disconnect","IGraphBuilder::Disconnect","dshow.ifiltergraph_disconnect","strmif/IFilterGraph::Disconnect","strmif/IGraphBuilder::Disconnect"]
old-location: dshow\ifiltergraph_disconnect.htm
tech.root: dshow
ms.assetid: 8c7d6cb6-b91c-4461-8f2b-38342a88eafc
ms.date: 12/05/2018
ms.keywords: Disconnect, Disconnect method [DirectShow], Disconnect method [DirectShow],IFilterGraph interface, Disconnect method [DirectShow],IGraphBuilder interface, IFilterGraph interface [DirectShow],Disconnect method, IFilterGraph.Disconnect, IFilterGraph::Disconnect, IFilterGraphDisconnect, IGraphBuilder interface [DirectShow],Disconnect method, IGraphBuilder.Disconnect, IGraphBuilder::Disconnect, dshow.ifiltergraph_disconnect, strmif/IFilterGraph::Disconnect, strmif/IGraphBuilder::Disconnect
f1_keywords:
- strmif/IFilterGraph.Disconnect
dev_langs:
- c++
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
- wmp.dll
api_name:
- IFilterGraph.Disconnect
- IGraphBuilder.Disconnect
- IGraphBuilder.Disconnect
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFilterGraph::Disconnect


## -description



The <code>Disconnect</code> method disconnects this pin.




## -parameters




### -param ppin [in]

Pointer to the pin to disconnect.


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
The filter is not stopped, but does not support reconnection while in a running state.

</td>
</tr>
</table>
 




## -remarks



This method does not completely break the connection. To completely break the connection, both ends must be disconnected.

To remove a filter from the filter graph entirely, call the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ifiltergraph-removefilter">IFilterGraph::RemoveFilter</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ifiltergraph">IFilterGraph Interface</a>
 

 

