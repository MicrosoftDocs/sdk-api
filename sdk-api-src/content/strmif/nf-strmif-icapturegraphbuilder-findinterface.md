---
UID: NF:strmif.ICaptureGraphBuilder.FindInterface
title: ICaptureGraphBuilder::FindInterface (strmif.h)
author: windows-sdk-content
description: Note  The ICaptureGraphBuilder interface is deprecated. Use ICaptureGraphBuilder2 instead. Looks for the specified interface on the filter, upstream and downstream from the filter, and, optionally, only on the output pin of the given category.
old-location: dshow\icapturegraphbuilder_findinterface.htm
tech.root: DirectShow
ms.assetid: 23fe9a5a-0f3b-44b3-9d37-6889214657bf
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FindInterface, FindInterface method [DirectShow], FindInterface method [DirectShow],ICaptureGraphBuilder interface, ICaptureGraphBuilder interface [DirectShow],FindInterface method, ICaptureGraphBuilder.FindInterface, ICaptureGraphBuilder::FindInterface, ICaptureGraphBuilderFindInterface, dshow.icapturegraphbuilder_findinterface, strmif/ICaptureGraphBuilder::FindInterface
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - ICaptureGraphBuilder.FindInterface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICaptureGraphBuilder::FindInterface


## -description



<div class="alert"><b>Note</b>  The <b>ICaptureGraphBuilder</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/abdf6fb2-e98f-4df8-98ec-06d33798abb5">ICaptureGraphBuilder2</a> instead.</div>
<div> </div>
Looks for the specified interface on the filter, upstream and downstream from the filter, and, optionally, only on the output pin of the given category.




## -parameters




### -param pCategory [in]

Pointer to a GUID specifying the output pin category. See <a href="https://msdn.microsoft.com/0c01bd51-353d-4f48-b33c-796f740915e2">Pin Property Set</a> for a list of all pin categories. <b>NULL</b> indicates search all the output pins regardless of category.


### -param pf [in]

Pointer to the <a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter</a> interface of the filter.


### -param riid [in]

Reference ID of the desired interface.


### -param ppint [out]

Address of a void pointer. If the interface was found, this method initializes <i>ppint</i> so that it contains the address of a pointer to the found interface. Call the <b>Release</b> method to decrement the reference count when you're done with the interface.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method looks for the interface on the filter, and upstream and downstream of the filter, unless a category is given. If a category is given, it only looks downstream of the output pin of that category. It can be used to find interfaces on renderers, multiplexers, TV tuners, crossbars, and so forth.

If <i>pCategory</i> equals &amp;LOOK_UPSTREAM_ONLY, then the graph builder will look upstream of the filter given in parameter <i>pf</i>, but not on the filter itself, nor downstream of the filter.

If <i>pCategory</i> equals &amp;LOOK_DOWNSTREAM_ONLY, then the graph builder will look downstream of the filter given in parameter <i>pf</i>, but not on the filter itself, nor upstream of the filter.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/64ee80cd-9f63-4f38-853a-1ecfc03e6076">ICaptureGraphBuilder Interface</a>
 

 

