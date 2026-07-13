---
UID: NF:dwrite_3.IDWriteRemoteFontFileStream.GetLocalFileSize
title: IDWriteRemoteFontFileStream::GetLocalFileSize (dwrite_3.h)
description: GetLocalFileSize returns the number of bytes of the font file that are currently local, which should always be less than or equal to the full file size returned by GetFileSize.
helpviewer_keywords: ["GetLocalFileSize","GetLocalFileSize method [Direct Write]","GetLocalFileSize method [Direct Write]","IDWriteRemoteFontFileStream interface","IDWriteRemoteFontFileStream interface [Direct Write]","GetLocalFileSize method","IDWriteRemoteFontFileStream.GetLocalFileSize","IDWriteRemoteFontFileStream::GetLocalFileSize","directwrite.idwriteremotefontfilestream_getlocalfilesize","dwrite_3/IDWriteRemoteFontFileStream::GetLocalFileSize"]
old-location: directwrite\idwriteremotefontfilestream_getlocalfilesize.htm
tech.root: DirectWrite
ms.assetid: 06FB14D5-19F6-48D3-AEA9-3D622219EF2A
ms.date: 09/10/2025
ms.keywords: GetLocalFileSize, GetLocalFileSize method [Direct Write], GetLocalFileSize method [Direct Write],IDWriteRemoteFontFileStream interface, IDWriteRemoteFontFileStream interface [Direct Write],GetLocalFileSize method, IDWriteRemoteFontFileStream.GetLocalFileSize, IDWriteRemoteFontFileStream::GetLocalFileSize, directwrite.idwriteremotefontfilestream_getlocalfilesize, dwrite_3/IDWriteRemoteFontFileStream::GetLocalFileSize
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
 - IDWriteRemoteFontFileStream::GetLocalFileSize
 - dwrite_3/IDWriteRemoteFontFileStream::GetLocalFileSize
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
 - IDWriteRemoteFontFileStream.GetLocalFileSize
---

# IDWriteRemoteFontFileStream::GetLocalFileSize


## -description

GetLocalFileSize returns the number of bytes of the font file that are currently local, which should always be less than or equal to the full
          file size returned by <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefontfilestream-getfilesize">GetFileSize</a>. 
         If the locality is remote, the return value is zero. If the file is fully local, the return value must be the
          same as <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefontfilestream-getfilesize">GetFileSize</a>.

## -parameters

### -param localFileSize [out]

Type: <b>UINT64*</b>

Receives the local size of the file.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream">IDWriteRemoteFontFileStream</a>

