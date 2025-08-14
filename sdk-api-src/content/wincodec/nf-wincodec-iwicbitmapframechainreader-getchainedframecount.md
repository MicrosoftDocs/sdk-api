---
UID: NF:wincodec.IWICBitmapFrameChainReader.GetChainedFrameCount
title: IWICBitmapFrameChainReader::GetChainedFrameCount
description: Retrieves the count of frames for a chain of a given type.
ms.date: 07/15/2025
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
 - IWICBitmapFrameChainReader::GetChainedFrameCount
f1_keywords:
 - IWICBitmapFrameChainReader::GetChainedFrameCount
 - wincodec/IWICBitmapFrameChainReader::GetChainedFrameCount
dev_langs:
 - c++
helpviewer_keywords:
 - GetChainedFrameCount
---

## -description

Retrieves the count of frames for a chain of a given type.

## -parameters

### -param chainType

Type: **[WICBitmapChainType](./ne-wincodec-wicbitmapchaintype)**

The chain type to query about.

### -param pCount

Type: **[UINT](/windows/win32/winprog/windows-data-types)\***

Receives the count of frames for chains of type *chainType*.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [HRESULT](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).

## -remarks

## -see-also
