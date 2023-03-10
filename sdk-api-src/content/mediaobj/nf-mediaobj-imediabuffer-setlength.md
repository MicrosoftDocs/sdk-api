---
UID: NF:mediaobj.IMediaBuffer.SetLength
title: IMediaBuffer::SetLength (mediaobj.h)
description: The SetLength method specifies the length of the data currently in the buffer.
helpviewer_keywords: ["IMediaBuffer interface [DirectShow]","SetLength method","IMediaBuffer.SetLength","IMediaBuffer::SetLength","IMediaBufferSetLength","SetLength","SetLength method [DirectShow]","SetLength method [DirectShow]","IMediaBuffer interface","dshow.imediabuffer_setlength","mediaobj/IMediaBuffer::SetLength"]
old-location: dshow\imediabuffer_setlength.htm
tech.root: dshow
ms.assetid: 06cfbfd3-d196-4adb-a6b3-9b5f88bc03a6
ms.date: 12/05/2018
ms.keywords: IMediaBuffer interface [DirectShow],SetLength method, IMediaBuffer.SetLength, IMediaBuffer::SetLength, IMediaBufferSetLength, SetLength, SetLength method [DirectShow], SetLength method [DirectShow],IMediaBuffer interface, dshow.imediabuffer_setlength, mediaobj/IMediaBuffer::SetLength
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
 - IMediaBuffer::SetLength
 - mediaobj/IMediaBuffer::SetLength
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
 - IMediaBuffer.SetLength
---

# IMediaBuffer::SetLength


## -description

The <code>SetLength</code> method specifies the length of the data currently in the buffer.

## -parameters

### -param cbLength

Size of the data, in bytes. The value must not exceed the buffer's maximum size. Call the <a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediabuffer-getmaxlength">IMediaBuffer::GetMaxLength</a> method to obtain the maximum size.

## -returns

Returns S_OK if successful. Otherwise, returns an <b>HRESULT</b> value indicating the cause of the error.

## -remarks

This method sets the size of the valid data currently in the buffer, not the buffer's allocated size.

## -see-also

<a href="/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer">IMediaBuffer Interface</a>



<a href="/windows/desktop/DirectShow/implementing-imediabuffer">Implementing IMediaBuffer</a>