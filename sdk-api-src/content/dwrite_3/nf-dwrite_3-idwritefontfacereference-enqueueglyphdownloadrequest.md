---
UID: NF:dwrite_3.IDWriteFontFaceReference.EnqueueGlyphDownloadRequest
title: IDWriteFontFaceReference::EnqueueGlyphDownloadRequest
author: windows-sdk-content
description: Adds a request to the font download queue (IDWriteFontDownloadQueue).
old-location: directwrite\idwritefontfacereference_enqueueglyphdownloadrequest.htm
tech.root: DirectWrite
ms.assetid: 4e35c011-8d5b-0bb5-fea2-4034b8e379aa
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: EnqueueGlyphDownloadRequest, EnqueueGlyphDownloadRequest method [Direct Write], EnqueueGlyphDownloadRequest method [Direct Write],IDWriteFontFaceReference interface, IDWriteFontFaceReference interface [Direct Write],EnqueueGlyphDownloadRequest method, IDWriteFontFaceReference.EnqueueGlyphDownloadRequest, IDWriteFontFaceReference::EnqueueGlyphDownloadRequest, directwrite.idwritefontfacereference_enqueueglyphdownloadrequest, dwrite_3/IDWriteFontFaceReference::EnqueueGlyphDownloadRequest
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
 - IDWriteFontFaceReference.EnqueueGlyphDownloadRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontFaceReference::EnqueueGlyphDownloadRequest


## -description


Adds a request to the font download queue (<a href="https://msdn.microsoft.com/d1b1dfab-a22a-40bb-ffc4-eb094ac14217">IDWriteFontDownloadQueue</a>).


## -parameters




### -param glyphIndices [in]

Type: <b>const UINT16*</b>

Array of glyph indices to download.


### -param glyphCount

Type: <b>UINT32</b>

The number of elements in the glyph index array.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Downloading a glyph involves downloading any other glyphs it depends on from the font tables (GSUB, COLR, glyf).




## -see-also




<a href="https://msdn.microsoft.com/04242508-7439-43B6-B3E7-07617B782038">IDWriteFontFaceReference</a>
 

 

