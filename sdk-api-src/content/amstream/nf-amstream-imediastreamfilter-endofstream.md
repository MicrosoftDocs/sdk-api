---
UID: NF:amstream.IMediaStreamFilter.EndOfStream
title: IMediaStreamFilter::EndOfStream (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The EndOfStream method signals the end of a stream. The Media Stream filter's input pins call this method on the filter.
helpviewer_keywords: ["EndOfStream","EndOfStream method [DirectShow]","EndOfStream method [DirectShow]","IMediaStreamFilter interface","IMediaStreamFilter interface [DirectShow]","EndOfStream method","IMediaStreamFilter.EndOfStream","IMediaStreamFilter::EndOfStream","IMediaStreamFilterEndOfStream","amstream/IMediaStreamFilter::EndOfStream","dshow.imediastreamfilter_endofstream"]
old-location: dshow\imediastreamfilter_endofstream.htm
tech.root: dshow
ms.assetid: ceec4ead-e439-4206-ab30-ae37d15c5b44
ms.date: 12/05/2018
ms.keywords: EndOfStream, EndOfStream method [DirectShow], EndOfStream method [DirectShow],IMediaStreamFilter interface, IMediaStreamFilter interface [DirectShow],EndOfStream method, IMediaStreamFilter.EndOfStream, IMediaStreamFilter::EndOfStream, IMediaStreamFilterEndOfStream, amstream/IMediaStreamFilter::EndOfStream, dshow.imediastreamfilter_endofstream
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
 - IMediaStreamFilter::EndOfStream
 - amstream/IMediaStreamFilter::EndOfStream
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
 - IMediaStreamFilter.EndOfStream
---

# IMediaStreamFilter::EndOfStream


## -description

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>EndOfStream</code> method signals the end of a stream. The Media Stream filter's input pins call this method on the filter.



## -returns

Returns S_OK if successful, or an error code otherwise.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-imediastreamfilter">IMediaStreamFilter Interface</a>
