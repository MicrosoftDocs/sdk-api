---
UID: NN:dwrite_3.IDWriteRemoteFontFileStream
title: IDWriteRemoteFontFileStream (dwrite_3.h)
description: Represents a font file stream, parts of which may be non-local.
helpviewer_keywords: ["IDWriteRemoteFontFileStream","IDWriteRemoteFontFileStream interface [Direct Write]","IDWriteRemoteFontFileStream interface [Direct Write]","described","directwrite.idwriteremotefontfilestream","dwrite_3/IDWriteRemoteFontFileStream"]
old-location: directwrite\idwriteremotefontfilestream.htm
tech.root: DirectWrite
ms.assetid: 2CC73CE0-162A-4808-ACB6-A9599FD4D09F
ms.date: 09/10/2025
ms.keywords: IDWriteRemoteFontFileStream, IDWriteRemoteFontFileStream interface [Direct Write], IDWriteRemoteFontFileStream interface [Direct Write],described, directwrite.idwriteremotefontfilestream, dwrite_3/IDWriteRemoteFontFileStream
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
 - IDWriteRemoteFontFileStream
 - dwrite_3/IDWriteRemoteFontFileStream
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
 - IDWriteRemoteFontFileStream
---

# IDWriteRemoteFontFileStream interface


## -description

Represents a font file stream, parts of which may be non-local.
          Non-local data must be downloaded before it can be accessed using
          ReadFragment. The interface exposes methods to download font data and query the locality of font data.

## -inheritance

The <b>IDWriteRemoteFontFileStream</b> interface inherits from <a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream">IDWriteFontFileStream</a>. <b>IDWriteRemoteFontFileStream</b> also has these types of members:

## -remarks

For more information, see the description of IDWriteRemoteFontFileLoader.

