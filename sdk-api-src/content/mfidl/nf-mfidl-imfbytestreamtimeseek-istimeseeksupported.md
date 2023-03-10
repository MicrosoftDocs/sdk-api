---
UID: NF:mfidl.IMFByteStreamTimeSeek.IsTimeSeekSupported
title: IMFByteStreamTimeSeek::IsTimeSeekSupported (mfidl.h)
description: Queries whether the byte stream supports time-based seeking.
helpviewer_keywords: ["IMFByteStreamTimeSeek interface [Media Foundation]","IsTimeSeekSupported method","IMFByteStreamTimeSeek.IsTimeSeekSupported","IMFByteStreamTimeSeek::IsTimeSeekSupported","IsTimeSeekSupported","IsTimeSeekSupported method [Media Foundation]","IsTimeSeekSupported method [Media Foundation]","IMFByteStreamTimeSeek interface","mf.imfbytestreamtimeseek_istimeseeksupported","mfidl/IMFByteStreamTimeSeek::IsTimeSeekSupported"]
old-location: mf\imfbytestreamtimeseek_istimeseeksupported.htm
tech.root: mf
ms.assetid: 92FCE0EF-046C-4639-958E-731795C5A123
ms.date: 12/05/2018
ms.keywords: IMFByteStreamTimeSeek interface [Media Foundation],IsTimeSeekSupported method, IMFByteStreamTimeSeek.IsTimeSeekSupported, IMFByteStreamTimeSeek::IsTimeSeekSupported, IsTimeSeekSupported, IsTimeSeekSupported method [Media Foundation], IsTimeSeekSupported method [Media Foundation],IMFByteStreamTimeSeek interface, mf.imfbytestreamtimeseek_istimeseeksupported, mfidl/IMFByteStreamTimeSeek::IsTimeSeekSupported
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFByteStreamTimeSeek::IsTimeSeekSupported
 - mfidl/IMFByteStreamTimeSeek::IsTimeSeekSupported
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFByteStreamTimeSeek.IsTimeSeekSupported
---

# IMFByteStreamTimeSeek::IsTimeSeekSupported


## -description

Queries whether the byte stream supports time-based seeking.

## -parameters

### -param pfTimeSeekIsSupported [out]

Receives the value <b>TRUE</b> if the byte stream supports time-based seeking, or <b>FALSE</b> otherwise.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamtimeseek">IMFByteStreamTimeSeek</a>