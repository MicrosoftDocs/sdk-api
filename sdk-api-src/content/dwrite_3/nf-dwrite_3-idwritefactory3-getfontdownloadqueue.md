---
UID: NF:dwrite_3.IDWriteFactory3.GetFontDownloadQueue
title: IDWriteFactory3::GetFontDownloadQueue (dwrite_3.h)
description: Gets the font download queue associated with this factory object.
helpviewer_keywords: ["GetFontDownloadQueue","GetFontDownloadQueue method [Direct Write]","GetFontDownloadQueue method [Direct Write]","IDWriteFactory3 interface","IDWriteFactory3 interface [Direct Write]","GetFontDownloadQueue method","IDWriteFactory3.GetFontDownloadQueue","IDWriteFactory3::GetFontDownloadQueue","directwrite.idwritefactory3_getfontdownloadqueue","dwrite_3/IDWriteFactory3::GetFontDownloadQueue"]
old-location: directwrite\idwritefactory3_getfontdownloadqueue.htm
tech.root: DirectWrite
ms.assetid: 446e4544-b25d-9b59-922c-ca5c896ea99f
ms.date: 09/10/2025
ms.keywords: GetFontDownloadQueue, GetFontDownloadQueue method [Direct Write], GetFontDownloadQueue method [Direct Write],IDWriteFactory3 interface, IDWriteFactory3 interface [Direct Write],GetFontDownloadQueue method, IDWriteFactory3.GetFontDownloadQueue, IDWriteFactory3::GetFontDownloadQueue, directwrite.idwritefactory3_getfontdownloadqueue, dwrite_3/IDWriteFactory3::GetFontDownloadQueue
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IDWriteFactory3::GetFontDownloadQueue
 - dwrite_3/IDWriteFactory3::GetFontDownloadQueue
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
 - IDWriteFactory3.GetFontDownloadQueue
---

# IDWriteFactory3::GetFontDownloadQueue


## -description

Gets the font download queue associated with this factory object.

## -parameters

### -param fontDownloadQueue [out]

Type: <b><a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue">IDWriteFontDownloadQueue</a>**</b>

Receives a pointer to the font download queue interface.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3">IDWriteFactory3</a>

