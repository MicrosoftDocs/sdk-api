---
UID: NF:mfobjects.IMFByteStream.GetLength
title: IMFByteStream::GetLength (mfobjects.h)
description: Retrieves the length of the stream.
helpviewer_keywords: ["6fb817a6-5b43-4716-a997-bbd8a0b9305d","GetLength","GetLength method [Media Foundation]","GetLength method [Media Foundation]","IMFByteStream interface","IMFByteStream interface [Media Foundation]","GetLength method","IMFByteStream.GetLength","IMFByteStream::GetLength","mf.imfbytestream_getlength","mfobjects/IMFByteStream::GetLength"]
old-location: mf\imfbytestream_getlength.htm
tech.root: mf
ms.assetid: 6fb817a6-5b43-4716-a997-bbd8a0b9305d
ms.date: 12/05/2018
ms.keywords: 6fb817a6-5b43-4716-a997-bbd8a0b9305d, GetLength, GetLength method [Media Foundation], GetLength method [Media Foundation],IMFByteStream interface, IMFByteStream interface [Media Foundation],GetLength method, IMFByteStream.GetLength, IMFByteStream::GetLength, mf.imfbytestream_getlength, mfobjects/IMFByteStream::GetLength
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFByteStream::GetLength
 - mfobjects/IMFByteStream::GetLength
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFByteStream.GetLength
---

# IMFByteStream::GetLength


## -description

Retrieves the length of the stream.

## -parameters

### -param pqwLength [out]

Receives the length of the stream, in bytes. If the length is unknown, this value is -1.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a>