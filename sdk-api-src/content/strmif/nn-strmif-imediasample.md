---
UID: NN:strmif.IMediaSample
title: IMediaSample (strmif.h)
description: The IMediaSample interface sets and retrieves properties on media samples.
helpviewer_keywords: ["IMediaSample","IMediaSample interface [DirectShow]","IMediaSample interface [DirectShow]","described","IMediaSampleInterface","dshow.imediasample","strmif/IMediaSample"]
old-location: dshow\imediasample.htm
tech.root: dshow
ms.assetid: 883e5e3b-db91-4806-96cc-c6f8cddfcca6
ms.date: 12/05/2018
ms.keywords: IMediaSample, IMediaSample interface [DirectShow], IMediaSample interface [DirectShow],described, IMediaSampleInterface, dshow.imediasample, strmif/IMediaSample
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
 - IMediaSample
 - strmif/IMediaSample
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
 - IMediaSample
---

# IMediaSample interface


## -description

The <code>IMediaSample</code> interface sets and retrieves properties on media samples. A media sample is a COM object that contains a block of media data. Media samples support the use of shared memory buffers among filters.

Typically, applications do not call methods on this interface. Filters use this interface to set properties on samples, and deliver the samples to a downstream filter. The downstream filter uses the interface to retrieve the properties and read the data. The filter can modify the data in place, or it can copy the sample, modify the copy, and pass the copy downstream.

The <a href="/windows/desktop/api/strmif/nn-strmif-imediasample2">IMediaSample2</a> interface inherits this interface.

## -inheritance

The <b>IMediaSample</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMediaSample</b> also has these types of members:

