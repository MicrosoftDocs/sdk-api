---
UID: NF:mfidl.MFCreateStreamOnMFByteStreamEx
title: MFCreateStreamOnMFByteStreamEx function (mfidl.h)
description: Creates an IRandomAccessStream object that wraps a Microsoft Media Foundation byte stream.
helpviewer_keywords: ["MFCreateStreamOnMFByteStreamEx","MFCreateStreamOnMFByteStreamEx function [Media Foundation]","mf.mfcreatestreamonmfbytestreamex","mf.mfcreatewinrtstreamonmfbytestream","mfidl/MFCreateStreamOnMFByteStreamEx"]
old-location: mf\mfcreatestreamonmfbytestreamex.htm
tech.root: mf
ms.assetid: 5D43889B-6430-4057-87E8-B8501B52E4A5
ms.date: 12/05/2018
ms.keywords: MFCreateStreamOnMFByteStreamEx, MFCreateStreamOnMFByteStreamEx function [Media Foundation], mf.mfcreatestreamonmfbytestreamex, mf.mfcreatewinrtstreamonmfbytestream, mfidl/MFCreateStreamOnMFByteStreamEx
req.header: mfidl.h
req.include-header: 
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateStreamOnMFByteStreamEx
 - mfidl/MFCreateStreamOnMFByteStreamEx
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
 - MFCreateStreamOnMFByteStreamEx
---

# MFCreateStreamOnMFByteStreamEx function


## -description

Creates an <a href="/previous-versions/hh438400(v=vs.85)">IRandomAccessStream</a> object that wraps a Microsoft Media Foundation byte stream.

## -parameters

### -param pByteStream [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> interface of the Media Foundation byte stream.

### -param riid [in]

The interface identifier (IID) of the interface being requested.

### -param ppv [out]

Receives a pointer to the requested interface. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The returned byte stream object exposes the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice">IMFGetService</a> interface. To get the original <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> pointer, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> using the service identifier <b>MF_WRAPPED_OBJECT</b>.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>