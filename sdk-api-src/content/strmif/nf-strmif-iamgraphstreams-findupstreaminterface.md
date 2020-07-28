---
UID: NF:strmif.IAMGraphStreams.FindUpstreamInterface
title: IAMGraphStreams::FindUpstreamInterface (strmif.h)
description: The FindUpstreamInterface method searches the filter graph for a specified interface, upstream from a specified pin.
helpviewer_keywords: ["FindUpstreamInterface","FindUpstreamInterface method [DirectShow]","FindUpstreamInterface method [DirectShow]","IAMGraphStreams interface","IAMGraphStreams interface [DirectShow]","FindUpstreamInterface method","IAMGraphStreams.FindUpstreamInterface","IAMGraphStreams::FindUpstreamInterface","IAMGraphStreamsFindUpstreamInterface","dshow.iamgraphstreams_findupstreaminterface","strmif/IAMGraphStreams::FindUpstreamInterface"]
old-location: dshow\iamgraphstreams_findupstreaminterface.htm
tech.root: dshow
ms.assetid: 23106ef0-e5ce-47a6-97b0-518bb78ec67c
ms.date: 12/05/2018
ms.keywords: FindUpstreamInterface, FindUpstreamInterface method [DirectShow], FindUpstreamInterface method [DirectShow],IAMGraphStreams interface, IAMGraphStreams interface [DirectShow],FindUpstreamInterface method, IAMGraphStreams.FindUpstreamInterface, IAMGraphStreams::FindUpstreamInterface, IAMGraphStreamsFindUpstreamInterface, dshow.iamgraphstreams_findupstreaminterface, strmif/IAMGraphStreams::FindUpstreamInterface
f1_keywords:
- strmif/IAMGraphStreams.FindUpstreamInterface
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
- IAMGraphStreams.FindUpstreamInterface
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMGraphStreams::FindUpstreamInterface


## -description



The <code>FindUpstreamInterface</code> method searches the filter graph for a specified interface, upstream from a specified pin.




## -parameters




### -param pPin [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ipin">IPin</a> interface of a pin. The pin must belong to a filter in the filter graph.


### -param riid [in]

Reference to an interface identifier (IID) that specifies the interface to find.


### -param ppvInterface [out]

Address of a void pointer. If the method succeeds, this variable receives a pointer to the interface specified by <i>riid</i>.


### -param dwFlags [in]

Combination of flags from the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-_am_intf_search_flags">AM_INTF_SEARCH_FLAGS</a> enumeration, specifying what to search (pins or filters).


## -returns



Returns one of the following <b>HRESULT</b> values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Interface not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
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
</table>
 




## -remarks



If <i>dwFlags</i> is zero, this method searches for the interface in the following order:

<ol>
<li>It queries the pin specified by <i>pPin</i>.</li>
<li>
If <i>pPin</i> is an input pin, it calls <b>FindUpstreamInterface</b> recursively on the output pin that is connected to <i>pPin</i>, if any.

If <i>pPin</i> is an output pin, it queries the filter that owns <i>pPin</i>. Then it creates a list of input pins on the filter that have internal connections to <i>pPin</i>, and calls <code>FindUpstreamInterface</code> recursively on those input pins.

To create a list of input pins with internal connections, the method does the following:

<ul>
<li>Calls <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipin-queryinternalconnections">IPin::QueryInternalConnections</a>.</li>
<li>If that fails, calls <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ibasefilter-enumpins">IBaseFilter::EnumPins</a> and looks for input pins.</li>
</ul>
</li>
</ol>
It stops at the first object it finds that supports the interface. You can limit the objects that are searched (filters, input pin, or output pins) by setting <i>dwFlags</i> to a non-zero value.

<div class="alert"><b>Note</b>  The <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder2-findinterface">ICaptureGraphBuilder2::FindInterface</a> method implements a more general approach to this problem, and in most situations is preferred.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamgraphstreams">IAMGraphStreams Interface</a>
 

 

