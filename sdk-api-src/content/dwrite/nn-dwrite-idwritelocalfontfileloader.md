---
UID: NN:dwrite.IDWriteLocalFontFileLoader
title: IDWriteLocalFontFileLoader (dwrite.h)
description: A built-in implementation of the IDWriteFontFileLoader interface, that operates on local font files and exposes local font file information from the font file reference key.
helpviewer_keywords: ["IDWriteLocalFontFileLoader","IDWriteLocalFontFileLoader interface [Direct Write]","IDWriteLocalFontFileLoader interface [Direct Write]","described","directwrite.idwritelocalfontfileloader","dwrite/IDWriteLocalFontFileLoader"]
old-location: directwrite\idwritelocalfontfileloader.htm
tech.root: DirectWrite
ms.assetid: acb777c8-24c6-452e-8f58-8fb2ad8c0b6c
ms.date: 12/05/2018
ms.keywords: IDWriteLocalFontFileLoader, IDWriteLocalFontFileLoader interface [Direct Write], IDWriteLocalFontFileLoader interface [Direct Write],described, directwrite.idwritelocalfontfileloader, dwrite/IDWriteLocalFontFileLoader
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IDWriteLocalFontFileLoader
 - dwrite/IDWriteLocalFontFileLoader
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
 - IDWriteLocalFontFileLoader
---

# IDWriteLocalFontFileLoader interface


## -description

A built-in implementation of the <a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader">IDWriteFontFileLoader</a> interface, that operates on local font files
and exposes local font file information from the font file reference key. Font file references created using <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference">CreateFontFileReference</a> use this font file loader.

## -inheritance

The <b>IDWriteLocalFontFileLoader</b> interface inherits from the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDWriteLocalFontFileLoader</b> also has these types of members:

