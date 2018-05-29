---
UID: NF:strmif.IFilterGraph.EnumFilters
title: IFilterGraph::EnumFilters
author: windows-sdk-content
description: The EnumFilters method provides an enumerator for all filters in the graph.
old-location: dshow\ifiltergraph_enumfilters.htm
old-project: DirectShow
ms.assetid: 3a6dcd1a-3ec3-4f0f-8e82-2d33ad775eec
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: EnumFilters, EnumFilters method [DirectShow], EnumFilters method [DirectShow],IFilterGraph interface, EnumFilters method [DirectShow],IGraphBuilder interface, IFilterGraph interface [DirectShow],EnumFilters method, IFilterGraph.EnumFilters, IFilterGraph::EnumFilters, IFilterGraphEnumFilters, IGraphBuilder interface [DirectShow],EnumFilters method, IGraphBuilder.EnumFilters, IGraphBuilder::EnumFilters, dshow.ifiltergraph_enumfilters, strmif/IFilterGraph::EnumFilters, strmif/IGraphBuilder::EnumFilters
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IFilterGraph.EnumFilters
-	IGraphBuilder.EnumFilters
-	IGraphBuilder.EnumFilters
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IFilterGraph::EnumFilters


## -description



The <code>EnumFilters</code> method provides an enumerator for all filters in the graph.




## -parameters




### -param ppEnum [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/e105ccff-86c6-45d5-aead-6d303d038e5a">IEnumFilters</a> interface. Use this interface to enumerate the filters. The caller must release the interface.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to create the enumerator.

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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/73a92f44-03c6-47e3-98d1-a20100ed8fa1">IFilterGraph Interface</a>
 

 

