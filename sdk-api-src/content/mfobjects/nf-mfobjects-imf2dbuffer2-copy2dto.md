---
UID: NF:mfobjects.IMF2DBuffer2.Copy2DTo
title: IMF2DBuffer2::Copy2DTo (mfobjects.h)
description: Copies the buffer to another 2D buffer object.
helpviewer_keywords: ["Copy2DTo","Copy2DTo method [Media Foundation]","Copy2DTo method [Media Foundation]","IMF2DBuffer2 interface","IMF2DBuffer2 interface [Media Foundation]","Copy2DTo method","IMF2DBuffer2.Copy2DTo","IMF2DBuffer2::Copy2DTo","mf.imf2dbuffer2_copy2dto","mfobjects/IMF2DBuffer2::Copy2DTo"]
old-location: mf\imf2dbuffer2_copy2dto.htm
tech.root: mf
ms.assetid: 90B0CBA2-2474-4B34-8BB4-6C59C05CDD7E
ms.date: 12/05/2018
ms.keywords: Copy2DTo, Copy2DTo method [Media Foundation], Copy2DTo method [Media Foundation],IMF2DBuffer2 interface, IMF2DBuffer2 interface [Media Foundation],Copy2DTo method, IMF2DBuffer2.Copy2DTo, IMF2DBuffer2::Copy2DTo, mf.imf2dbuffer2_copy2dto, mfobjects/IMF2DBuffer2::Copy2DTo
req.header: mfobjects.h
req.include-header: Mfidl.h
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
 - IMF2DBuffer2::Copy2DTo
 - mfobjects/IMF2DBuffer2::Copy2DTo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfobjects.h
api_name:
 - IMF2DBuffer2.Copy2DTo
---

# IMF2DBuffer2::Copy2DTo


## -description

Copies the buffer to another 2D buffer object.

## -parameters

### -param pDestBuffer [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer2">IMF2DBuffer2</a> interface of the destination buffer.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The destination buffer must be at least as large as the source buffer.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer2">IMF2DBuffer2</a>