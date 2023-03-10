---
UID: NN:mfidl.IMFByteStreamTimeSeek
title: IMFByteStreamTimeSeek (mfidl.h)
description: Seeks a byte stream by time position.
helpviewer_keywords: ["IMFByteStreamTimeSeek","IMFByteStreamTimeSeek interface [Media Foundation]","IMFByteStreamTimeSeek interface [Media Foundation]","described","mf.imfbytestreamtimeseek","mfidl/IMFByteStreamTimeSeek"]
old-location: mf\imfbytestreamtimeseek.htm
tech.root: mf
ms.assetid: BD9EDFF7-46BA-4788-A44E-C69C4B0BEB50
ms.date: 12/05/2018
ms.keywords: IMFByteStreamTimeSeek, IMFByteStreamTimeSeek interface [Media Foundation], IMFByteStreamTimeSeek interface [Media Foundation],described, mf.imfbytestreamtimeseek, mfidl/IMFByteStreamTimeSeek
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IMFByteStreamTimeSeek
 - mfidl/IMFByteStreamTimeSeek
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFByteStreamTimeSeek
---

# IMFByteStreamTimeSeek interface


## -description

Seeks a byte stream by time position.

## -inheritance

The <b>IMFByteStreamTimeSeek</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFByteStreamTimeSeek</b> also has these types of members:

## -remarks

A byte stream can implement this interface if it supports time-based seeking. For example, a byte stream that reads data from a server  might implement the interface. Typically, a local file-based byte stream would not implement it.

To get a pointer to this interface, call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the byte stream object.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
