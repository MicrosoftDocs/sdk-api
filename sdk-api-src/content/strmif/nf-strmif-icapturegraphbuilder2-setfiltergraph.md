---
UID: NF:strmif.ICaptureGraphBuilder2.SetFiltergraph
title: ICaptureGraphBuilder2::SetFiltergraph
author: windows-sdk-content
description: The SetFiltergraph method specifies a filter graph for the capture graph builder to use.
old-location: dshow\icapturegraphbuilder2_setfiltergraph.htm
old-project: DirectShow
ms.assetid: 6193ece8-cdf1-44f5-9619-16380352193f
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: ICaptureGraphBuilder2 interface [DirectShow],SetFiltergraph method, ICaptureGraphBuilder2.SetFiltergraph, ICaptureGraphBuilder2::SetFiltergraph, ICaptureGraphBuilder2SetFiltergraph, SetFiltergraph, SetFiltergraph method [DirectShow], SetFiltergraph method [DirectShow],ICaptureGraphBuilder2 interface, dshow.icapturegraphbuilder2_setfiltergraph, strmif/ICaptureGraphBuilder2::SetFiltergraph
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.redist: 
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
 - ICaptureGraphBuilder2.SetFiltergraph
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# ICaptureGraphBuilder2::SetFiltergraph


## -description



The <code>SetFiltergraph</code> method specifies a filter graph for the capture graph builder to use.




## -parameters




### -param pfg [in]

Pointer to the filter graph's <a href="https://msdn.microsoft.com/54ed8ac8-4821-4c0c-9fb9-789c70dbca37">IGraphBuilder</a> interface.


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
Unexpected error.

</td>
</tr>
</table>
 




## -remarks



If you do not call this method, the capture graph builder automatically creates a filter graph when it needs one. If the capture graph builder already has a filter graph, this method returns E_UNEXPECTED.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/abdf6fb2-e98f-4df8-98ec-06d33798abb5">ICaptureGraphBuilder2 Interface</a>
 

 

