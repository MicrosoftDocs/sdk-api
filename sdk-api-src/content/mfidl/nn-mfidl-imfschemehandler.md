---
UID: NN:mfidl.IMFSchemeHandler
title: IMFSchemeHandler (mfidl.h)
description: Creates a media source or a byte stream from a URL.
helpviewer_keywords: ["IMFSchemeHandler","IMFSchemeHandler interface [Media Foundation]","IMFSchemeHandler interface [Media Foundation]","described","a342054e-2cb5-494a-a2f7-d144c72d1fa5","mf.imfschemehandler","mfidl/IMFSchemeHandler"]
old-location: mf\imfschemehandler.htm
tech.root: mf
ms.assetid: a342054e-2cb5-494a-a2f7-d144c72d1fa5
ms.date: 12/05/2018
ms.keywords: IMFSchemeHandler, IMFSchemeHandler interface [Media Foundation], IMFSchemeHandler interface [Media Foundation],described, a342054e-2cb5-494a-a2f7-d144c72d1fa5, mf.imfschemehandler, mfidl/IMFSchemeHandler
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
 - IMFSchemeHandler
 - mfidl/IMFSchemeHandler
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
 - IMFSchemeHandler
---

# IMFSchemeHandler interface


## -description

Creates a media source or a byte stream from a URL.

## -inheritance

The <b>IMFSchemeHandler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSchemeHandler</b> also has these types of members:

## -remarks

Applications do not use this interface. This interface is exposed by scheme handlers, which are used by the source resolver. A scheme handler is designed to parse one type of URL scheme. When the scheme handler is given a URL, it parses the resource that is located at that URL and creates either a media source or a byte stream.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/scheme-handlers-and-byte-stream-handlers">Scheme Handlers and Byte-Stream Handlers</a>
