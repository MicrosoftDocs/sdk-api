---
UID: NF:dwrite_3.IDWriteFontFaceReference.EnqueueCharacterDownloadRequest
title: IDWriteFontFaceReference::EnqueueCharacterDownloadRequest
author: windows-sdk-content
description: Adds a request to the font download queue (IDWriteFontDownloadQueue).
old-location: directwrite\idwritefontfacereference_enqueuecharacterdownloadrequest.htm
tech.root: DirectWrite
ms.assetid: 7ca1b6c7-46c2-2440-35e4-0bcdc375d74e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: EnqueueCharacterDownloadRequest, EnqueueCharacterDownloadRequest method [Direct Write], EnqueueCharacterDownloadRequest method [Direct Write],IDWriteFontFaceReference interface, IDWriteFontFaceReference interface [Direct Write],EnqueueCharacterDownloadRequest method, IDWriteFontFaceReference.EnqueueCharacterDownloadRequest, IDWriteFontFaceReference::EnqueueCharacterDownloadRequest, directwrite.idwritefontfacereference_enqueuecharacterdownloadrequest, dwrite_3/IDWriteFontFaceReference::EnqueueCharacterDownloadRequest
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFontFaceReference.EnqueueCharacterDownloadRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontFaceReference::EnqueueCharacterDownloadRequest


## -description


Adds a request to the font download queue (<a href="https://msdn.microsoft.com/d1b1dfab-a22a-40bb-ffc4-eb094ac14217">IDWriteFontDownloadQueue</a>).


## -parameters




### -param characters [in]

Type: <b>const WCHAR*</b>

Array of characters to download.


### -param characterCount

Type: <b>UINT32</b>

The number of elements in the character array.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 Downloading a character involves downloading every glyph it depends on directly or indirectly, via font tables (cmap, GSUB, COLR, glyf).




## -see-also




<a href="https://msdn.microsoft.com/04242508-7439-43B6-B3E7-07617B782038">IDWriteFontFaceReference</a>
 

 

