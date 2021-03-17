---
UID: NF:strmif.IAMGraphBuilderCallback.CreatedFilter
title: IAMGraphBuilderCallback::CreatedFilter (strmif.h)
description: The Filter Graph Manager calls this method after it has created a filter, but before it attempts to connect the filter.
helpviewer_keywords: ["CreatedFilter","CreatedFilter method [DirectShow]","CreatedFilter method [DirectShow]","IAMGraphBuilderCallback interface","IAMGraphBuilderCallback interface [DirectShow]","CreatedFilter method","IAMGraphBuilderCallback.CreatedFilter","IAMGraphBuilderCallback::CreatedFilter","IAMGraphBuilderCallbackCreatedFilter","dshow.iamgraphbuildercallback_createdfilter","strmif/IAMGraphBuilderCallback::CreatedFilter"]
old-location: dshow\iamgraphbuildercallback_createdfilter.htm
tech.root: dshow
ms.assetid: 04a20a3f-a4a5-434b-896a-60d36430f390
ms.date: 12/05/2018
ms.keywords: CreatedFilter, CreatedFilter method [DirectShow], CreatedFilter method [DirectShow],IAMGraphBuilderCallback interface, IAMGraphBuilderCallback interface [DirectShow],CreatedFilter method, IAMGraphBuilderCallback.CreatedFilter, IAMGraphBuilderCallback::CreatedFilter, IAMGraphBuilderCallbackCreatedFilter, dshow.iamgraphbuildercallback_createdfilter, strmif/IAMGraphBuilderCallback::CreatedFilter
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMGraphBuilderCallback::CreatedFilter
 - strmif/IAMGraphBuilderCallback::CreatedFilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMGraphBuilderCallback.CreatedFilter
---

# IAMGraphBuilderCallback::CreatedFilter


## -description

The Filter Graph Manager calls this method after it has created a filter, but before it attempts to connect the filter.

## -parameters

### -param pFil

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface of the filter.

## -returns

If the method returns a success code, the Filter Graph Manager tries to connect the filter. If the method returns a failure code, the Filter Graph Manager rejects the filter.

## -remarks

This method enables the client to configure the filter immediately after it has been created. The Video Mixing Renderer is the primary example of a filter that requires configuration before it is connected. Most other DirectShow filters can be configured after they are connected.

The Filter Graph Manager holds a graph-wide critical section while it calls this method. Therefore, the callback method should avoid calling any methods on the Filter Graph Manager, or any methods on filters that might change the graph state (such as disconnecting pins). Doing so might cause a deadlock or other unexpected behaviors.

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-iamgraphbuildercallback">IAMGraphBuilderCallback Interface</a>