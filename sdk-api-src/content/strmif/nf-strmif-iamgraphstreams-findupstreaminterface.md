---
UID: NF:strmif.IAMGraphStreams.FindUpstreamInterface
title: IAMGraphStreams::FindUpstreamInterface
author: windows-sdk-content
description: The FindUpstreamInterface method searches the filter graph for a specified interface, upstream from a specified pin.
old-location: dshow\iamgraphstreams_findupstreaminterface.htm
tech.root: DirectShow
ms.assetid: 23106ef0-e5ce-47a6-97b0-518bb78ec67c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FindUpstreamInterface, FindUpstreamInterface method [DirectShow], FindUpstreamInterface method [DirectShow],IAMGraphStreams interface, IAMGraphStreams interface [DirectShow],FindUpstreamInterface method, IAMGraphStreams.FindUpstreamInterface, IAMGraphStreams::FindUpstreamInterface, IAMGraphStreamsFindUpstreamInterface, dshow.iamgraphstreams_findupstreaminterface, strmif/IAMGraphStreams::FindUpstreamInterface
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMGraphStreams::FindUpstreamInterface


## -description



The <code>FindUpstreamInterface</code> method searches the filter graph for a specified interface, upstream from a specified pin.




## -parameters




### -param pPin [in]

Pointer to the <a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin</a> interface of a pin. The pin must belong to a filter in the filter graph.


### -param riid [in]

Reference to an interface identifier (IID) that specifies the interface to find.


### -param ppvInterface [out]

Address of a void pointer. If the method succeeds, this variable receives a pointer to the interface specified by <i>riid</i>.


### -param dwFlags [in]

Combination of flags from the <a href="https://msdn.microsoft.com/090c19c8-eb38-4185-9f6b-169495f9ab27">AM_INTF_SEARCH_FLAGS</a> enumeration, specifying what to search (pins or filters).


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
<li>Calls <a href="https://msdn.microsoft.com/c0289b89-9220-402c-858c-09076e2ab6b6">IPin::QueryInternalConnections</a>.</li>
<li>If that fails, calls <a href="https://msdn.microsoft.com/02675c93-7901-40f6-a9fc-f6f13f56acca">IBaseFilter::EnumPins</a> and looks for input pins.</li>
</ul>
</li>
</ol>
It stops at the first object it finds that supports the interface. You can limit the objects that are searched (filters, input pin, or output pins) by setting <i>dwFlags</i> to a non-zero value.

<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/931b42bf-25d6-4f0a-8c45-baf8ed65e302">ICaptureGraphBuilder2::FindInterface</a> method implements a more general approach to this problem, and in most situations is preferred.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/30d44536-2a2d-44ab-bafc-bdb851cd272b">IAMGraphStreams Interface</a>
 

 

