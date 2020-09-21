---
UID: NF:amstream.IAMMediaStream.JoinFilterGraph
title: IAMMediaStream::JoinFilterGraph (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The JoinFilterGraph method connects a media stream filter to a filter graph.
helpviewer_keywords: ["IAMMediaStream interface [DirectShow]","JoinFilterGraph method","IAMMediaStream.JoinFilterGraph","IAMMediaStream::JoinFilterGraph","IAMMediaStreamJoinFilterGraph","JoinFilterGraph","JoinFilterGraph method [DirectShow]","JoinFilterGraph method [DirectShow]","IAMMediaStream interface","amstream/IAMMediaStream::JoinFilterGraph","dshow.iammediastream_joinfiltergraph"]
old-location: dshow\iammediastream_joinfiltergraph.htm
tech.root: dshow
ms.assetid: b14e9be4-f292-4a71-b541-4fda2640591d
ms.date: 12/05/2018
ms.keywords: IAMMediaStream interface [DirectShow],JoinFilterGraph method, IAMMediaStream.JoinFilterGraph, IAMMediaStream::JoinFilterGraph, IAMMediaStreamJoinFilterGraph, JoinFilterGraph, JoinFilterGraph method [DirectShow], JoinFilterGraph method [DirectShow],IAMMediaStream interface, amstream/IAMMediaStream::JoinFilterGraph, dshow.iammediastream_joinfiltergraph
req.header: amstream.h
req.include-header: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMMediaStream::JoinFilterGraph
 - amstream/IAMMediaStream::JoinFilterGraph
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - amstream.h
api_name:
 - IAMMediaStream.JoinFilterGraph
---

# IAMMediaStream::JoinFilterGraph


## -description

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>JoinFilterGraph</code> method connects a media stream filter to a filter graph.

## -parameters

### -param pFilterGraph [in]

Pointer to the current media stream filter to add to the specified filter graph.

## -returns

Returns S_OK if successful or E_POINTER if <i>pGraph</i> is <b>NULL</b>.

## -remarks

Don't increment the reference count of the specified filter graph.

Applications should not call this method.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammediastream">IAMMediaStream Interface</a>