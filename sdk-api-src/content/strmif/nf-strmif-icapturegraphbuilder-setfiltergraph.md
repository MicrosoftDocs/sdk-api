---
UID: NF:strmif.ICaptureGraphBuilder.SetFiltergraph
title: ICaptureGraphBuilder::SetFiltergraph
author: windows-sdk-content
description: Note  The ICaptureGraphBuilder interface is deprecated. Use ICaptureGraphBuilder2 instead. Tells the graph builder object which filter graph to use.
old-location: dshow\icapturegraphbuilder_setfiltergraph.htm
old-project: DirectShow
ms.assetid: 01cb7f09-6ff2-46c1-b6f2-76583785b242
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: ICaptureGraphBuilder interface [DirectShow],SetFiltergraph method, ICaptureGraphBuilder.SetFiltergraph, ICaptureGraphBuilder::SetFiltergraph, ICaptureGraphBuilderSetFiltergraph, SetFiltergraph, SetFiltergraph method [DirectShow], SetFiltergraph method [DirectShow],ICaptureGraphBuilder interface, dshow.icapturegraphbuilder_setfiltergraph, strmif/ICaptureGraphBuilder::SetFiltergraph
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.redist: 
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - ICaptureGraphBuilder.SetFiltergraph
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# ICaptureGraphBuilder::SetFiltergraph


## -description



<div class="alert"><b>Note</b>  The <b>ICaptureGraphBuilder</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/abdf6fb2-e98f-4df8-98ec-06d33798abb5">ICaptureGraphBuilder2</a> instead.</div>
<div> </div>
Tells the graph builder object which filter graph to use.




## -parameters




### -param pfg [in]

Pointer to an <a href="https://msdn.microsoft.com/54ed8ac8-4821-4c0c-9fb9-789c70dbca37">IGraphBuilder</a> interface that specifies the filter graph to use for subsequent calls to the <a href="https://msdn.microsoft.com/8f837917-015f-427f-b234-b0ccbcf943eb">IFilterGraph::AddFilter</a> method.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



The graph builder will automatically create a filter graph if you don't call this method. If you call this method after the graph builder has created its own filter graph, the call will fail.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/64ee80cd-9f63-4f38-853a-1ecfc03e6076">ICaptureGraphBuilder Interface</a>
 

 

