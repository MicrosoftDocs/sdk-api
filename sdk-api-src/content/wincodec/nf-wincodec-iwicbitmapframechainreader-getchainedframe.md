---
UID: NF:wincodec.IWICBitmapFrameChainReader.GetChainedFrame
title: IWICBitmapFrameChainReader::GetChainedFrame
description: Retrieves a frame for a chain of a given type.
ms.date: 07/14/2025
tech.root: wic
targetos: Windows
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: wincodec.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - wincodec.h
api_name:
 - IWICBitmapFrameChainReader::GetChainedFrame
f1_keywords:
 - IWICBitmapFrameChainReader::GetChainedFrame
 - wincodec/IWICBitmapFrameChainReader::GetChainedFrame
dev_langs:
 - c++
helpviewer_keywords:
 - GetChainedFrame
---

## -description

Retrieves a frame for a chain of a given type.

## -parameters

### -param chainType

Type: **[WICBitmapChainType](./ne-wincodec-wicbitmapchaintype)**

The chain type for which to retrieve a frame.

### -param index

Type: **[UINT](/windows/win32/winprog/windows-data-types)**

The index of the frame to retrieve.

### -param ppIBitmapFrame

Type: **[IWICBitmapFrameDecode](./nn-wincodec-iwicbitmapframedecode.md)\*\***

Receives the frame at *index* for chains of type *chainType*.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [HRESULT](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).

## -remarks

## -see-also
