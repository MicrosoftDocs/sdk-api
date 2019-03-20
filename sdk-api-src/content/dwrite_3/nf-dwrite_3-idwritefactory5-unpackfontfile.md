---
UID: NF:dwrite_3.IDWriteFactory5.UnpackFontFile
title: IDWriteFactory5::UnpackFontFile (dwrite_3.h)
author: windows-sdk-content
description: The UnpackFontFile method unpacks font data from a container file (WOFF or WOFF2) and returns the unpacked font data in the form of a font file stream.
old-location: directwrite\idwritefactory5_unpackfontfile.htm
tech.root: DirectWrite
ms.assetid: F82863DC-BFC8-49D3-93C5-DCA45093F81A
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDWriteFactory5 interface [Direct Write],UnpackFontFile method, IDWriteFactory5.UnpackFontFile, IDWriteFactory5::UnpackFontFile, UnpackFontFile, UnpackFontFile method [Direct Write], UnpackFontFile method [Direct Write],IDWriteFactory5 interface, directwrite.idwritefactory5_unpackfontfile, dwrite_3/IDWriteFactory5::UnpackFontFile
ms.topic: method
req.header: dwrite_3.h
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dwrite.lib
 - Dwrite.dll
api_name:
 - IDWriteFactory5.UnpackFontFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFactory5::UnpackFontFile


## -description


The UnpackFontFile method unpacks font data from a container file (WOFF or WOFF2) and returns the unpacked font data in the form of a font file stream.


## -parameters




### -param containerType

Type: <b><a href="https://msdn.microsoft.com/93275F1D-A25C-4BDD-B278-DA56ADB3436D">DWRITE_CONTAINER_TYPE</a></b>

Container type returned by AnalyzeContainerType.


### -param fileData [in]

Type: <b>void</b>

Pointer to the compressed data.


### -param fileDataSize

Type: <b>UINT32</b>

Size of the compressed data, in bytes.


### -param unpackedFontStream [out]

Type: <b><a href="https://msdn.microsoft.com/792ab9be-853f-427d-a762-2da8e81423f8">IDWriteFontFileStream</a>**</b>

Receives a pointer to a newly created font file stream containing the uncompressed data.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Standard HRESULT error code. The return value is E_INVALIDARG if the container type is DWRITE_CONTAINER_TYPE_UNKNOWN.




## -see-also




<a href="https://msdn.microsoft.com/2F3E30DC-A965-4C68-A337-73F338CF2563">IDWriteFactory5</a>
 

 

