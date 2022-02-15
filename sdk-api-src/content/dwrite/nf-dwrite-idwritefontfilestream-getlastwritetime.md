---
UID: NF:dwrite.IDWriteFontFileStream.GetLastWriteTime
title: IDWriteFontFileStream::GetLastWriteTime (dwrite.h)
description: Obtains the last modified time of the file.
helpviewer_keywords: ["GetLastWriteTime","GetLastWriteTime method [Direct Write]","GetLastWriteTime method [Direct Write]","IDWriteFontFileStream interface","IDWriteFontFileStream interface [Direct Write]","GetLastWriteTime method","IDWriteFontFileStream.GetLastWriteTime","IDWriteFontFileStream::GetLastWriteTime","directwrite.IDWriteFontFileStream_GetLastWriteTime","dwrite/IDWriteFontFileStream::GetLastWriteTime"]
old-location: directwrite\IDWriteFontFileStream_GetLastWriteTime.htm
tech.root: DirectWrite
ms.assetid: eb4045c0-a333-40aa-8ec3-b89cfd835be3
ms.date: 12/05/2018
ms.keywords: GetLastWriteTime, GetLastWriteTime method [Direct Write], GetLastWriteTime method [Direct Write],IDWriteFontFileStream interface, IDWriteFontFileStream interface [Direct Write],GetLastWriteTime method, IDWriteFontFileStream.GetLastWriteTime, IDWriteFontFileStream::GetLastWriteTime, directwrite.IDWriteFontFileStream_GetLastWriteTime, dwrite/IDWriteFontFileStream::GetLastWriteTime
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteFontFileStream::GetLastWriteTime
 - dwrite/IDWriteFontFileStream::GetLastWriteTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFontFileStream.GetLastWriteTime
---

# IDWriteFontFileStream::GetLastWriteTime


## -description

 Obtains the last modified time of the file.

## -parameters

### -param lastWriteTime [out]

Type: <b>UINT64*</b>

When this method returns, contains  the last modified time of the file in the format that represents
     the number of 100-nanosecond intervals since January 1, 1601 (UTC).

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The "last modified time" is used by DirectWrite font selection algorithms
     to determine whether one font resource is more up to date than another one.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream">IDWriteFontFileStream</a>

