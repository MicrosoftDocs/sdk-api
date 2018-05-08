---
UID: NF:strmif.ICaptureGraphBuilder.GetFiltergraph
title: ICaptureGraphBuilder::GetFiltergraph
author: windows-driver-content
description: Note  The ICaptureGraphBuilder interface is deprecated. Use ICaptureGraphBuilder2 instead. Retrieves the filter graph that the builder is using.
old-location: dshow\icapturegraphbuilder_getfiltergraph.htm
old-project: DirectShow
ms.assetid: 9cb43dca-79f1-4467-8e17-6f2a0b4db785
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: GetFiltergraph, GetFiltergraph method [DirectShow], GetFiltergraph method [DirectShow],ICaptureGraphBuilder interface, ICaptureGraphBuilder interface [DirectShow],GetFiltergraph method, ICaptureGraphBuilder.GetFiltergraph, ICaptureGraphBuilder::GetFiltergraph, ICaptureGraphBuilderGetFiltergraph, dshow.icapturegraphbuilder_getfiltergraph, strmif/ICaptureGraphBuilder::GetFiltergraph
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmif.h
api_name:
-	ICaptureGraphBuilder.GetFiltergraph
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# ICaptureGraphBuilder::GetFiltergraph


## -description



<div class="alert"><b>Note</b>  The <b>ICaptureGraphBuilder</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/abdf6fb2-e98f-4df8-98ec-06d33798abb5">ICaptureGraphBuilder2</a> instead.</div>
<div> </div>
Retrieves the filter graph that the builder is using.




## -parameters




### -param ppfg [out]

Address of a pointer to an <a href="https://msdn.microsoft.com/54ed8ac8-4821-4c0c-9fb9-789c70dbca37">IGraphBuilder</a> interface.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method increments the reference count on the <a href="https://msdn.microsoft.com/54ed8ac8-4821-4c0c-9fb9-789c70dbca37">IGraphBuilder</a> interface; be sure to decrement the reference count on <b>IGraphBuilder</b> by calling the <b>Release</b> method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/64ee80cd-9f63-4f38-853a-1ecfc03e6076">ICaptureGraphBuilder Interface</a>
 

 

