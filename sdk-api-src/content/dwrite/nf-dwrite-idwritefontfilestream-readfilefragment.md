---
UID: NF:dwrite.IDWriteFontFileStream.ReadFileFragment
title: IDWriteFontFileStream::ReadFileFragment (dwrite.h)
description: Reads a fragment from a font file.
helpviewer_keywords: ["IDWriteFontFileStream interface [Direct Write]","ReadFileFragment method","IDWriteFontFileStream.ReadFileFragment","IDWriteFontFileStream::ReadFileFragment","ReadFileFragment","ReadFileFragment method [Direct Write]","ReadFileFragment method [Direct Write]","IDWriteFontFileStream interface","directwrite.IDWriteFontFileStream_ReadFileFragment","dwrite/IDWriteFontFileStream::ReadFileFragment"]
old-location: directwrite\IDWriteFontFileStream_ReadFileFragment.htm
tech.root: DirectWrite
ms.assetid: b5bf3300-cfa0-43db-b513-6c0d695c564e
ms.date: 12/05/2018
ms.keywords: IDWriteFontFileStream interface [Direct Write],ReadFileFragment method, IDWriteFontFileStream.ReadFileFragment, IDWriteFontFileStream::ReadFileFragment, ReadFileFragment, ReadFileFragment method [Direct Write], ReadFileFragment method [Direct Write],IDWriteFontFileStream interface, directwrite.IDWriteFontFileStream_ReadFileFragment, dwrite/IDWriteFontFileStream::ReadFileFragment
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
 - IDWriteFontFileStream::ReadFileFragment
 - dwrite/IDWriteFontFileStream::ReadFileFragment
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
 - IDWriteFontFileStream.ReadFileFragment
---

# IDWriteFontFileStream::ReadFileFragment


## -description

 Reads a fragment from a font file.

## -parameters

### -param fragmentStart [out]

Type: <b>const void**</b>

When this method returns, contains an address of a  pointer to the start of the font file fragment.  This parameter is passed uninitialized.

### -param fileOffset

Type: <b>UINT64</b>

The offset of the fragment, in bytes, from the beginning of the font file.

### -param fragmentSize

Type: <b>UINT64</b>

The size of the file fragment, in bytes.

### -param fragmentContext [out]

Type: <b>void**</b>

When this method returns, contains the address of a pointer to a pointer to the client-defined context to be passed to <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefontfilestream-releasefilefragment">ReleaseFileFragment</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 Note that <b>ReadFileFragment</b> implementations must check whether the requested font file fragment
     is within the file bounds. Otherwise, an error should be returned from <b>ReadFileFragment</b>.


<a href="/windows/win32/DirectWrite/direct-write-portal">DirectWrite</a> may invoke <a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream">IDWriteFontFileStream</a> methods on the same object from multiple threads simultaneously. Therefore, <b>ReadFileFragment</b> implementations that rely on internal mutable state must serialize access to such state across multiple threads. For example, an implementation that uses separate Seek and Read operations to read a file fragment must place the code block containing Seek and Read calls under a lock or a critical section.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream">IDWriteFontFileStream</a>

