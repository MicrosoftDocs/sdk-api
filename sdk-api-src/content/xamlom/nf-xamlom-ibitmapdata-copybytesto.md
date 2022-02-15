---
UID: NF:xamlom.IBitmapData.CopyBytesTo
title: IBitmapData::CopyBytesTo (xamlom.h)
description: Copies up to the specified maximum number of bytes from the given offset in the bitmap data into the caller’s buffer (pvBytes), and returns the number of bytes copied.
helpviewer_keywords: ["CopyBytesTo","CopyBytesTo method","CopyBytesTo method","IBitmapData interface","IBitmapData interface","CopyBytesTo method","IBitmapData.CopyBytesTo","IBitmapData::CopyBytesTo","xaml_diagnostics.ibitmapdata_copybytesto","xamlom/IBitmapData::CopyBytesTo"]
old-location: xaml_diagnostics\ibitmapdata_copybytesto.htm
tech.root: xaml_diagnostics
ms.assetid: 8E8CB014-D394-4457-8AC7-773A87EE2643
ms.date: 12/05/2018
ms.keywords: CopyBytesTo, CopyBytesTo method, CopyBytesTo method,IBitmapData interface, IBitmapData interface,CopyBytesTo method, IBitmapData.CopyBytesTo, IBitmapData::CopyBytesTo, xaml_diagnostics.ibitmapdata_copybytesto, xamlom/IBitmapData::CopyBytesTo
req.header: xamlom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XamlOM.idl
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
 - IBitmapData::CopyBytesTo
 - xamlom/IBitmapData::CopyBytesTo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xamlom.h
api_name:
 - IBitmapData.CopyBytesTo
---

# IBitmapData::CopyBytesTo


## -description

Copies up to the specified maximum number of bytes from the given offset in the bitmap data into the caller’s buffer (<i>pvBytes</i>), and returns the number of bytes copied.

## -parameters

### -param sourceOffsetInBytes [in]

The place in the bitmap data to start copying from, in bytes.

### -param maxBytesToCopy [in]

The maximum number of bytes to copy.

### -param pvBytes [out]

The buffer into which the bytes are copied.

### -param numberOfBytesCopied [out]

The number of bytes copied.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ibitmapdata">IBitmapData</a>