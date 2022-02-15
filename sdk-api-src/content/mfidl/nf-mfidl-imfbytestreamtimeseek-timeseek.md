---
UID: NF:mfidl.IMFByteStreamTimeSeek.TimeSeek
title: IMFByteStreamTimeSeek::TimeSeek (mfidl.h)
description: Seeks to a new position in the byte stream.
helpviewer_keywords: ["IMFByteStreamTimeSeek interface [Media Foundation]","TimeSeek method","IMFByteStreamTimeSeek.TimeSeek","IMFByteStreamTimeSeek::TimeSeek","TimeSeek","TimeSeek method [Media Foundation]","TimeSeek method [Media Foundation]","IMFByteStreamTimeSeek interface","mf.imfbytestreamtimeseek_timeseek","mfidl/IMFByteStreamTimeSeek::TimeSeek"]
old-location: mf\imfbytestreamtimeseek_timeseek.htm
tech.root: mf
ms.assetid: 786F1299-A9E2-4B2C-A6AE-F88E6BF022DC
ms.date: 12/05/2018
ms.keywords: IMFByteStreamTimeSeek interface [Media Foundation],TimeSeek method, IMFByteStreamTimeSeek.TimeSeek, IMFByteStreamTimeSeek::TimeSeek, TimeSeek, TimeSeek method [Media Foundation], TimeSeek method [Media Foundation],IMFByteStreamTimeSeek interface, mf.imfbytestreamtimeseek_timeseek, mfidl/IMFByteStreamTimeSeek::TimeSeek
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
 - IMFByteStreamTimeSeek::TimeSeek
 - mfidl/IMFByteStreamTimeSeek::TimeSeek
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
 - IMFByteStreamTimeSeek.TimeSeek
---

# IMFByteStreamTimeSeek::TimeSeek


## -description

Seeks to a new position in the byte stream.

## -parameters

### -param qwTimePosition

The new position, in 100-nanosecond units.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the byte stream reads from a server, it might cache the seek request until the next read request. Therefore, the byte stream might not send a request to the server immediately.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamtimeseek">IMFByteStreamTimeSeek</a>