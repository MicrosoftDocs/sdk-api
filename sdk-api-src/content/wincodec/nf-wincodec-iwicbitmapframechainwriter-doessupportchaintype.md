---
UID: NF:wincodec.IWICBitmapFrameChainWriter.DoesSupportChainType
title: IWICBitmapFrameChainWriter::DoesSupportChainType
description: Determines whether the specified chain type is supported.
ms.date: 07/17/2025
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
 - IWICBitmapFrameChainWriter::DoesSupportChainType
f1_keywords:
 - IWICBitmapFrameChainWriter::DoesSupportChainType
 - wincodec/IWICBitmapFrameChainWriter::DoesSupportChainType
dev_langs:
 - c++
helpviewer_keywords:
 - DoesSupportChainType
---

## -description

Determines whether the specified chain type is supported.

## -parameters

### -param chainType

Type: **[WICBitmapChainType](./ne-wincodec-wicbitmapchaintype)**

The specified chain type to query about.

### -param pfIsSupported

Type: **[BOOL](/windows/win32/winprog/windows-data-types)\***

Used to retrieve a value indicating whether the chain type specified in *chainType* is supported. **TRUE** if it's supported; otherwise, **FALSE**.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [HRESULT](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).

## -remarks

## -see-also
