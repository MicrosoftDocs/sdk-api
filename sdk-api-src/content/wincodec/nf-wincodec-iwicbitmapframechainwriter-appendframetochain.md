---
UID: NF:wincodec.IWICBitmapFrameChainWriter.AppendFrameToChain
title: IWICBitmapFrameChainWriter::AppendFrameToChain
description: Creates a frame that's linked to a chain of a given type.
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
 - IWICBitmapFrameChainWriter::AppendFrameToChain
f1_keywords:
 - IWICBitmapFrameChainWriter::AppendFrameToChain
 - wincodec/IWICBitmapFrameChainWriter::AppendFrameToChain
dev_langs:
 - c++
helpviewer_keywords:
 - AppendFrameToChain
---

## -description

Creates a frame that's linked to a chain of a given type.

## -parameters

### -param chainType

Type: **[WICBitmapChainType](./ne-wincodec-wicbitmapchaintype)**

The chain type to link the new frame to.

### -param ppIFrameEncode

Type: **[IWICBitmapFrameEncode](./nn-wincodec-iwicbitmapframeencode.md)\*\***

Receives the new frame for a chain of type *chainType*.

### -param ppIEncoderOptions

Type: **[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\*\***

Optional. Receives the named properties to use for subsequent frame initialization. For more info, see the **Remarks** in the [IWICBitmapEncoder::CreateNewFrame](./nf-wincodec-iwicbitmapencoder-createnewframe.md) topic.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [HRESULT](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).

## -remarks

## -see-also
