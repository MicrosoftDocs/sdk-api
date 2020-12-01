---
UID: NF:mediaobj.IMediaBuffer.GetMaxLength
title: IMediaBuffer::GetMaxLength (mediaobj.h)
description: The GetMaxLength method retrieves the maximum number of bytes this buffer can hold.
helpviewer_keywords: ["GetMaxLength","GetMaxLength method [DirectShow]","GetMaxLength method [DirectShow]","IMediaBuffer interface","IMediaBuffer interface [DirectShow]","GetMaxLength method","IMediaBuffer.GetMaxLength","IMediaBuffer::GetMaxLength","IMediaBufferGetMaxLength","dshow.imediabuffer_getmaxlength","mediaobj/IMediaBuffer::GetMaxLength"]
old-location: dshow\imediabuffer_getmaxlength.htm
tech.root: dshow
ms.assetid: 9e312d3b-4994-4493-861c-cc0f6f112362
ms.date: 12/05/2018
ms.keywords: GetMaxLength, GetMaxLength method [DirectShow], GetMaxLength method [DirectShow],IMediaBuffer interface, IMediaBuffer interface [DirectShow],GetMaxLength method, IMediaBuffer.GetMaxLength, IMediaBuffer::GetMaxLength, IMediaBufferGetMaxLength, dshow.imediabuffer_getmaxlength, mediaobj/IMediaBuffer::GetMaxLength
req.header: mediaobj.h
req.include-header: Dmo.h
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
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMediaBuffer::GetMaxLength
 - mediaobj/IMediaBuffer::GetMaxLength
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaBuffer.GetMaxLength
---

# IMediaBuffer::GetMaxLength


## -description

The <code>GetMaxLength</code> method retrieves the maximum number of bytes this buffer can hold.

## -parameters

### -param pcbMaxLength [out]

Pointer to a variable that receives the buffer's maximum size, in bytes.

## -returns

Returns S_OK if successful. Otherwise, returns an <b>HRESULT</b> value indicating the cause of the error.

## -see-also

<a href="/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer">IMediaBuffer Interface</a>



<a href="/windows/desktop/DirectShow/implementing-imediabuffer">Implementing IMediaBuffer</a>