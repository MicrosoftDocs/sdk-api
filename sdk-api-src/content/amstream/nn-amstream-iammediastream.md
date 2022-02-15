---
UID: NN:amstream.IAMMediaStream
title: IAMMediaStream (amstream.h)
description: Note  This interface is deprecated.
helpviewer_keywords: ["IAMMediaStream","IAMMediaStream interface [DirectShow]","IAMMediaStream interface [DirectShow]","described","IAMMediaStreamInterface","amstream/IAMMediaStream","dshow.iammediastream"]
old-location: dshow\iammediastream.htm
tech.root: dshow
ms.assetid: 14185e7d-d08d-4fd8-a255-075eaf12a708
ms.date: 12/05/2018
ms.keywords: IAMMediaStream, IAMMediaStream interface [DirectShow], IAMMediaStream interface [DirectShow],described, IAMMediaStreamInterface, amstream/IAMMediaStream, dshow.iammediastream
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
 - IAMMediaStream
 - amstream/IAMMediaStream
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
 - IAMMediaStream
---

# IAMMediaStream interface


## -description

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>IAMMediaStream</code> interface handles the internal connections between Microsoft DirectShow filters and filter graphs in applications that use multimedia streaming. This enables applications to automatically negotiate the transfer and conversion of data from the source to the application without having to write code to handle the connection, transfer of data, data conversion, and actual data rendering or file storage. This provides a uniform and predictable method of data access and control.

This interface isn't intended for implementation or use by application developers.

## -inheritance

The <b>IAMMediaStream</b> interface inherits from <a href="/windows/desktop/api/mmstream/nn-mmstream-imediastream">IMediaStream</a>. <b>IAMMediaStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/mmstream/nn-mmstream-imediastream">IMediaStream</a>
