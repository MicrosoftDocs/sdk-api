---
UID: NF:strmif.ICaptureGraphBuilder2.GetFiltergraph
title: ICaptureGraphBuilder2::GetFiltergraph
author: windows-sdk-content
description: The GetFiltergraph method retrieves the filter graph that the capture graph builder is using.
old-location: dshow\icapturegraphbuilder2_getfiltergraph.htm
old-project: DirectShow
ms.assetid: 91136a71-cfda-4aa5-ba6c-d1ce6cbef3c1
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetFiltergraph, GetFiltergraph method [DirectShow], GetFiltergraph method [DirectShow],ICaptureGraphBuilder2 interface, ICaptureGraphBuilder2 interface [DirectShow],GetFiltergraph method, ICaptureGraphBuilder2.GetFiltergraph, ICaptureGraphBuilder2::GetFiltergraph, ICaptureGraphBuilder2GetFiltergraph, dshow.icapturegraphbuilder2_getfiltergraph, strmif/ICaptureGraphBuilder2::GetFiltergraph
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
 - ICaptureGraphBuilder2.GetFiltergraph
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# ICaptureGraphBuilder2::GetFiltergraph


## -description



The <code>GetFiltergraph</code> method retrieves the filter graph that the capture graph builder is using.




## -parameters




### -param ppfg [out]

Receives an <a href="https://msdn.microsoft.com/54ed8ac8-4821-4c0c-9fb9-789c70dbca37">IGraphBuilder</a> interface pointer.


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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
No filter graph.

</td>
</tr>
</table>
 




## -remarks



Initially, the capture graph builder does not hold a pointer to a filter graph. This method returns E_UNEXPECTED until one of the following methods has been called:

<ul>
<li>
<a href="https://msdn.microsoft.com/2fb5f13c-2bf5-463b-a209-77129a159bd6">ICaptureGraphBuilder2::RenderStream</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6193ece8-cdf1-44f5-9619-16380352193f">ICaptureGraphBuilder2::SetFiltergraph</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b81a79c1-a6f2-4c80-ae86-095fb9f78673">ICaptureGraphBuilder2::SetOutputFileName</a>
</li>
</ul>
This method increments the reference count on the <b>IGraphBuilder</b> interface. Be sure to release the interface when you are done with it.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/abdf6fb2-e98f-4df8-98ec-06d33798abb5">ICaptureGraphBuilder2 Interface</a>
 

 

