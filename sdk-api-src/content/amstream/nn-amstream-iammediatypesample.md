---
UID: NN:amstream.IAMMediaTypeSample
title: IAMMediaTypeSample (amstream.h)
description: Note  This interface is deprecated.
helpviewer_keywords: ["IAMMediaTypeSample","IAMMediaTypeSample interface [DirectShow]","IAMMediaTypeSample interface [DirectShow]","described","IAMMediaTypeSampleInterface","amstream/IAMMediaTypeSample","dshow.iammediatypesample"]
old-location: dshow\iammediatypesample.htm
tech.root: dshow
ms.assetid: e0a62251-68ee-4318-b09a-0aac6b73bf54
ms.date: 12/05/2018
ms.keywords: IAMMediaTypeSample, IAMMediaTypeSample interface [DirectShow], IAMMediaTypeSample interface [DirectShow],described, IAMMediaTypeSampleInterface, amstream/IAMMediaTypeSample, dshow.iammediatypesample
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
 - IAMMediaTypeSample
 - amstream/IAMMediaTypeSample
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
 - IAMMediaTypeSample
---

# IAMMediaTypeSample interface


## -description

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
This interface contains methods for manipulating stream samples with arbitrary media types. Call the <a href="/windows/desktop/api/amstream/nf-amstream-iammediatypestream-createsample">IAMMediaTypeStream::CreateSample</a> method to create a sample that exposes this interface.

The methods in this interface parallel those of the <a href="/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample</a> interface, although <b>IAMMediaTypeSample</b> contains a <a href="/windows/desktop/api/amstream/nf-amstream-iammediatypesample-setpointer">SetPointer</a> method in addition to the <a href="/windows/desktop/api/amstream/nf-amstream-iammediatypesample-getpointer">GetPointer</a> method.

## -inheritance

The <b>IAMMediaTypeSample</b> interface inherits from <a href="/windows/desktop/api/mmstream/nn-mmstream-istreamsample">IStreamSample</a>. <b>IAMMediaTypeSample</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/mmstream/nn-mmstream-istreamsample">IStreamSample</a>
