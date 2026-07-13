---
UID: NF:dwrite_3.IDWriteRemoteFontFileLoader.CreateRemoteStreamFromKey
title: IDWriteRemoteFontFileLoader::CreateRemoteStreamFromKey (dwrite_3.h)
description: Creates a remote font file stream object that encapsulates an open file resource and can be used to download remote file data.
helpviewer_keywords: ["CreateRemoteStreamFromKey","CreateRemoteStreamFromKey method [Direct Write]","CreateRemoteStreamFromKey method [Direct Write]","IDWriteRemoteFontFileLoader interface","IDWriteRemoteFontFileLoader interface [Direct Write]","CreateRemoteStreamFromKey method","IDWriteRemoteFontFileLoader.CreateRemoteStreamFromKey","IDWriteRemoteFontFileLoader::CreateRemoteStreamFromKey","directwrite.idwriteremotefontfileloader_createremotestreamfromkey","dwrite_3/IDWriteRemoteFontFileLoader::CreateRemoteStreamFromKey"]
old-location: directwrite\idwriteremotefontfileloader_createremotestreamfromkey.htm
tech.root: DirectWrite
ms.assetid: 434B7349-0FD3-492F-8973-600A0A0DFA7B
ms.date: 09/10/2025
ms.keywords: CreateRemoteStreamFromKey, CreateRemoteStreamFromKey method [Direct Write], CreateRemoteStreamFromKey method [Direct Write],IDWriteRemoteFontFileLoader interface, IDWriteRemoteFontFileLoader interface [Direct Write],CreateRemoteStreamFromKey method, IDWriteRemoteFontFileLoader.CreateRemoteStreamFromKey, IDWriteRemoteFontFileLoader::CreateRemoteStreamFromKey, directwrite.idwriteremotefontfileloader_createremotestreamfromkey, dwrite_3/IDWriteRemoteFontFileLoader::CreateRemoteStreamFromKey
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 15063
req.target-min-winversvr: Windows 10 Build 15063
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteRemoteFontFileLoader::CreateRemoteStreamFromKey
 - dwrite_3/IDWriteRemoteFontFileLoader::CreateRemoteStreamFromKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dwrite.lib
 - Dwrite.dll
api_name:
 - IDWriteRemoteFontFileLoader.CreateRemoteStreamFromKey
---

# IDWriteRemoteFontFileLoader::CreateRemoteStreamFromKey


## -description

Creates a remote font file stream object that encapsulates an open file resource and can be used to download remote file data.

## -parameters

### -param fontFileReferenceKey [in]

Type: <b>void</b>

Font file reference key that uniquely identifies the font file resource within the scope of the font loader being used.

### -param fontFileReferenceKeySize

Type: <b>UINT32</b>

Size of font file reference key in bytes.

### -param fontFileStream [out]

Type: <b><a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream">IDWriteRemoteFontFileStream</a>**</b>

Pointer to the newly created font file stream.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -remarks

Unlike <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefontfileloader-createstreamfromkey">CreateStreamFromKey</a>, this method can be used to create a stream for a remote file. 
        If the file is remote, the client must call <a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwriteremotefontfilestream-begindownload">IDWriteRemoteFontFileStream::BeginDownload</a> with an empty array 
        of file fragments before the stream can be used to get the file size or access data.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader">IDWriteRemoteFontFileLoader</a>

