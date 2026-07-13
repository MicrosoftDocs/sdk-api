---
UID: NF:mfobjects.IMFByteStream.SetLength
title: IMFByteStream::SetLength (mfobjects.h)
description: Sets the length of the stream.
helpviewer_keywords: ["55bee595-0a32-4b9e-8b22-48fdb2913dfc","IMFByteStream interface [Media Foundation]","SetLength method","IMFByteStream.SetLength","IMFByteStream::SetLength","SetLength","SetLength method [Media Foundation]","SetLength method [Media Foundation]","IMFByteStream interface","mf.imfbytestream_setlength","mfobjects/IMFByteStream::SetLength"]
old-location: mf\imfbytestream_setlength.htm
tech.root: mf
ms.assetid: 55bee595-0a32-4b9e-8b22-48fdb2913dfc
ms.date: 12/05/2018
ms.keywords: 55bee595-0a32-4b9e-8b22-48fdb2913dfc, IMFByteStream interface [Media Foundation],SetLength method, IMFByteStream.SetLength, IMFByteStream::SetLength, SetLength, SetLength method [Media Foundation], SetLength method [Media Foundation],IMFByteStream interface, mf.imfbytestream_setlength, mfobjects/IMFByteStream::SetLength
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
 - IMFByteStream::SetLength
 - mfobjects/IMFByteStream::SetLength
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
 - IMFByteStream.SetLength
---

# IMFByteStream::SetLength


## -description

Sets the length of the stream.

## -parameters

### -param qwLength [in]

Length of the stream in bytes.

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