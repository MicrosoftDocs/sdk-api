---
UID: NF:dwrite_3.IDWriteFontFaceReference.EnqueueFileFragmentDownloadRequest
title: IDWriteFontFaceReference::EnqueueFileFragmentDownloadRequest
author: windows-sdk-content
description: Adds a request to the font download queue (IDWriteFontDownloadQueue).
old-location: directwrite\idwritefontfacereference_enqueuefilefragmentdownloadrequest.htm
old-project: DirectWrite
ms.assetid: 6dfc2793-7960-5c13-950d-9ba14900c3e0
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: EnqueueFileFragmentDownloadRequest, EnqueueFileFragmentDownloadRequest method [Direct Write], EnqueueFileFragmentDownloadRequest method [Direct Write],IDWriteFontFaceReference interface, IDWriteFontFaceReference interface [Direct Write],EnqueueFileFragmentDownloadRequest method, IDWriteFontFaceReference.EnqueueFileFragmentDownloadRequest, IDWriteFontFaceReference::EnqueueFileFragmentDownloadRequest, directwrite.idwritefontfacereference_enqueuefilefragmentdownloadrequest, dwrite_3/IDWriteFontFaceReference::EnqueueFileFragmentDownloadRequest
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dwrite_3.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFontFaceReference.EnqueueFileFragmentDownloadRequest
product: Windows
targetos: Windows
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDWriteFontFaceReference::EnqueueFileFragmentDownloadRequest


## -description


Adds a request to the font download queue (<a href="https://msdn.microsoft.com/d1b1dfab-a22a-40bb-ffc4-eb094ac14217">IDWriteFontDownloadQueue</a>).


## -parameters




### -param fileOffset

Type: <b>UINT64</b>

Offset of the fragment from the beginning of the font file.


### -param fragmentSize

Type: <b>UINT64</b>

Size of the fragment in bytes.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/04242508-7439-43B6-B3E7-07617B782038">IDWriteFontFaceReference</a>
 

 

