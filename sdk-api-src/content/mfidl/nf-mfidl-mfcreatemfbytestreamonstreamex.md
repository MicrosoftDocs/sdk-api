---
UID: NF:mfidl.MFCreateMFByteStreamOnStreamEx
title: MFCreateMFByteStreamOnStreamEx function (mfidl.h)
description: Creates a Microsoft Media Foundation byte stream that wraps an IRandomAccessStream object.
helpviewer_keywords: ["MFCreateMFByteStreamOnStreamEx","MFCreateMFByteStreamOnStreamEx function [Media Foundation]","mf.mfcreatemfbytestreamonstreamex","mf.mfcreatemfbytestreamonwinrtstream","mfidl/MFCreateMFByteStreamOnStreamEx"]
old-location: mf\mfcreatemfbytestreamonstreamex.htm
tech.root: mf
ms.assetid: C16C2A5D-7373-4EA9-A02C-3AF97EA47D34
ms.date: 12/05/2018
ms.keywords: MFCreateMFByteStreamOnStreamEx, MFCreateMFByteStreamOnStreamEx function [Media Foundation], mf.mfcreatemfbytestreamonstreamex, mf.mfcreatemfbytestreamonwinrtstream, mfidl/MFCreateMFByteStreamOnStreamEx
f1_keywords:
- mfidl/MFCreateMFByteStreamOnStreamEx
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- mfplat.dll
api_name:
- MFCreateMFByteStreamOnStreamEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFCreateMFByteStreamOnStreamEx function


## -description


Creates a Microsoft Media Foundation byte stream that wraps an <a href="https://docs.microsoft.com/previous-versions/hh438400(v=vs.85)">IRandomAccessStream</a> object.


## -parameters




### -param punkStream [in]

A pointer to the <a href="https://docs.microsoft.com/previous-versions/hh438400(v=vs.85)">IRandomAccessStream</a> interface.


### -param ppByteStream [out]

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 

