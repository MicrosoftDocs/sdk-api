---
UID: NF:mfidl.MFCreateStreamOnMFByteStream
title: MFCreateStreamOnMFByteStream function (mfidl.h)
description: Returns an IStream pointer that wraps a Microsoft Media Foundation byte stream.
helpviewer_keywords: ["MFCreateStreamOnMFByteStream","MFCreateStreamOnMFByteStream function [Media Foundation]","mf.mfcreatestreamonmfbytestream","mfidl/MFCreateStreamOnMFByteStream"]
old-location: mf\mfcreatestreamonmfbytestream.htm
tech.root: mf
ms.assetid: 97C72B89-2E57-494E-AEB8-41125B3D740E
ms.date: 12/05/2018
ms.keywords: MFCreateStreamOnMFByteStream, MFCreateStreamOnMFByteStream function [Media Foundation], mf.mfcreatestreamonmfbytestream, mfidl/MFCreateStreamOnMFByteStream
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - MFCreateStreamOnMFByteStream
 - mfidl/MFCreateStreamOnMFByteStream
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
 - MFCreateStreamOnMFByteStream
---

# MFCreateStreamOnMFByteStream function


## -description

Returns an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> pointer that wraps a Microsoft Media Foundation byte stream.

## -parameters

### -param pByteStream [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> interface of the Media Foundation byte stream.

### -param ppStream [out]

Receives a pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function enables an application to pass a Media Foundation byte stream to an API that takes an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> pointer.

## -see-also

<a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatemfbytestreamonstream">MFCreateMFByteStreamOnStream</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>