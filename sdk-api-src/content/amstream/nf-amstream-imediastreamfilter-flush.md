---
UID: NF:amstream.IMediaStreamFilter.Flush
title: IMediaStreamFilter::Flush (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The Flush method notifies the filter that one of its pins has flushed data. The filter's input pins call this method.
helpviewer_keywords: ["Flush","Flush method [DirectShow]","Flush method [DirectShow]","IMediaStreamFilter interface","IMediaStreamFilter interface [DirectShow]","Flush method","IMediaStreamFilter.Flush","IMediaStreamFilter::Flush","IMediaStreamFilterFlush","amstream/IMediaStreamFilter::Flush","dshow.imediastreamfilter_flush"]
old-location: dshow\imediastreamfilter_flush.htm
tech.root: dshow
ms.assetid: 30b5d8f7-e3ab-48e4-aefe-3b3e04aba638
ms.date: 12/05/2018
ms.keywords: Flush, Flush method [DirectShow], Flush method [DirectShow],IMediaStreamFilter interface, IMediaStreamFilter interface [DirectShow],Flush method, IMediaStreamFilter.Flush, IMediaStreamFilter::Flush, IMediaStreamFilterFlush, amstream/IMediaStreamFilter::Flush, dshow.imediastreamfilter_flush
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
 - IMediaStreamFilter::Flush
 - amstream/IMediaStreamFilter::Flush
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
 - IMediaStreamFilter.Flush
---

# IMediaStreamFilter::Flush


## -description

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>Flush</code> method notifies the filter that one of its pins has flushed data. The filter's input pins call this method.

## -parameters

### -param bCancelEOS [in]

Boolean value that indicates whether to cancel the pin's previous end-of-stream notification. If <b>TRUE</b>, the filter decrements the internal end-of-stream count.

## -returns

Returns S_OK if successful, or an error code otherwise.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-imediastreamfilter">IMediaStreamFilter Interface</a>