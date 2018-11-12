---
UID: NF:dwrite_3.IDWriteRemoteFontFileStream.GetFileFragmentLocality
title: IDWriteRemoteFontFileStream::GetFileFragmentLocality
author: windows-sdk-content
description: Returns information about the locality of a byte range (i.e., font fragment) within the font file stream.
old-location: directwrite\idwriteremotefontfilestream_getfilefragmentlocality.htm
tech.root: DirectWrite
ms.assetid: 24F68EFD-D4D6-442B-97C1-C639F570F56B
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetFileFragmentLocality, GetFileFragmentLocality method [Direct Write], GetFileFragmentLocality method [Direct Write],IDWriteRemoteFontFileStream interface, IDWriteRemoteFontFileStream interface [Direct Write],GetFileFragmentLocality method, IDWriteRemoteFontFileStream.GetFileFragmentLocality, IDWriteRemoteFontFileStream::GetFileFragmentLocality, directwrite.idwriteremotefontfilestream_getfilefragmentlocality, dwrite_3/IDWriteRemoteFontFileStream::GetFileFragmentLocality
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDWriteRemoteFontFileStream.GetFileFragmentLocality
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteRemoteFontFileStream::GetFileFragmentLocality


## -description


Returns information about the locality of a byte range (i.e., font fragment) within the font file stream.


## -parameters




### -param fileOffset

Type: <b>UINT64</b>

Offset of the fragment from the beginning of the font file.


### -param fragmentSize

Type: <b>UINT64</b>

Size of the fragment in bytes.


### -param isLocal [out]

Type: <b>BOOL*</b>

Receives TRUE if the first byte of the fragment is local, FALSE if not.


### -param partialSize

Type: <b>UINT64*</b>

Receives the number of contiguous bytes from the start of the fragment that have the same locality as the first byte.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -see-also




<a href="https://msdn.microsoft.com/2CC73CE0-162A-4808-ACB6-A9599FD4D09F">IDWriteRemoteFontFileStream</a>
 

 

