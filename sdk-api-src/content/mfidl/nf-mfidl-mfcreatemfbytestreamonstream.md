---
UID: NF:mfidl.MFCreateMFByteStreamOnStream
title: MFCreateMFByteStreamOnStream function (mfidl.h)
description: Creates a Microsoft Media Foundation byte stream that wraps an IStream pointer.
helpviewer_keywords: ["MFCreateMFByteStreamOnStream","MFCreateMFByteStreamOnStream function [Media Foundation]","mf.mfcreatemfbytestreamonstream","mfidl/MFCreateMFByteStreamOnStream"]
old-location: mf\mfcreatemfbytestreamonstream.htm
tech.root: mf
ms.assetid: 5ffd370a-ccc5-4229-b214-e07847287415
ms.date: 12/05/2018
ms.keywords: MFCreateMFByteStreamOnStream, MFCreateMFByteStreamOnStream function [Media Foundation], mf.mfcreatemfbytestreamonstream, mfidl/MFCreateMFByteStreamOnStream
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateMFByteStreamOnStream
 - mfidl/MFCreateMFByteStreamOnStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateMFByteStreamOnStream
---

# MFCreateMFByteStreamOnStream function


## -description

Creates a Microsoft Media Foundation byte stream that wraps an <b>IStream</b> pointer.

## -parameters

### -param pStream [in]

A pointer to the <b>IStream</b> interface.

### -param ppByteStream [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> interface. The caller must release the interface.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

This function enables applications to pass an <b>IStream</b> object to a Media Foundation API that takes an <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> pointer.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>