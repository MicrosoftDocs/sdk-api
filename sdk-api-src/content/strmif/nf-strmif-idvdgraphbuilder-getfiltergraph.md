---
UID: NF:strmif.IDvdGraphBuilder.GetFiltergraph
title: IDvdGraphBuilder::GetFiltergraph
author: windows-sdk-content
description: The GetFiltergraph method retrieves the IGraphBuilder interface for the filter graph used by the DVD-Video graph builder object.
old-location: dshow\idvdgraphbuilder_getfiltergraph.htm
tech.root: DirectShow
ms.assetid: 1f12140b-d10d-47d9-8bac-33fab084bff4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetFiltergraph, GetFiltergraph method [DirectShow], GetFiltergraph method [DirectShow],IDvdGraphBuilder interface, IDvdGraphBuilder interface [DirectShow],GetFiltergraph method, IDvdGraphBuilder.GetFiltergraph, IDvdGraphBuilder::GetFiltergraph, IDvdGraphBuilderGetFiltergraph, dshow.idvdgraphbuilder_getfiltergraph, strmif/IDvdGraphBuilder::GetFiltergraph
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
 - IDvdGraphBuilder.GetFiltergraph
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdGraphBuilder::GetFiltergraph


## -description



The <code>GetFiltergraph</code> method retrieves the <a href="https://msdn.microsoft.com/54ed8ac8-4821-4c0c-9fb9-789c70dbca37">IGraphBuilder</a> interface for the filter graph used by the DVD-Video graph builder object.




## -parameters




### -param ppGB [out]

Address of a pointer to the <a href="https://msdn.microsoft.com/54ed8ac8-4821-4c0c-9fb9-789c70dbca37">IGraphBuilder</a> interface that the DVD-Video graph builder object is using.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface. The current DirectShow implementation returns E_INVALIDARG if <i>ppGB</i> is invalid.




## -remarks



The returned <b>IGraphBuilder</b> interface pointer has an outstanding reference count. The caller must release the interface.




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/2179e54a-c6e2-4837-9f89-be210bde9180">IDvdGraphBuilder Interface</a>
 

 

