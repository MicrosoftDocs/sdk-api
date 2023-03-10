---
UID: NN:mfidl.IMFByteStreamHandler
title: IMFByteStreamHandler (mfidl.h)
description: Creates a media source from a byte stream.
helpviewer_keywords: ["80c402d4-8246-42ee-a981-69c8d605cb0f","IMFByteStreamHandler","IMFByteStreamHandler interface [Media Foundation]","IMFByteStreamHandler interface [Media Foundation]","described","mf.imfbytestreamhandler","mfidl/IMFByteStreamHandler"]
old-location: mf\imfbytestreamhandler.htm
tech.root: mf
ms.assetid: 80c402d4-8246-42ee-a981-69c8d605cb0f
ms.date: 12/05/2018
ms.keywords: 80c402d4-8246-42ee-a981-69c8d605cb0f, IMFByteStreamHandler, IMFByteStreamHandler interface [Media Foundation], IMFByteStreamHandler interface [Media Foundation],described, mf.imfbytestreamhandler, mfidl/IMFByteStreamHandler
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFByteStreamHandler
 - mfidl/IMFByteStreamHandler
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFByteStreamHandler
---

# IMFByteStreamHandler interface


## -description

Creates a media source from a byte stream.

## -inheritance

The <b>IMFByteStreamHandler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFByteStreamHandler</b> also has these types of members:

## -remarks

Applications do not use this interface directly. This interface is exposed by byte-stream handlers, which are used by the source resolver. When the byte-stream handler is given a byte stream, it parses the stream and creates a media source. Byte-stream handlers are registered by file name extension or MIME type.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/scheme-handlers-and-byte-stream-handlers">Scheme Handlers and Byte-Stream Handlers</a>
