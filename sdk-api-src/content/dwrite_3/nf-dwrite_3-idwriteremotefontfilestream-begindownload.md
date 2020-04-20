---
UID: NF:dwrite_3.IDWriteRemoteFontFileStream.BeginDownload
title: IDWriteRemoteFontFileStream::BeginDownload (dwrite_3.h)
description: Begins downloading all or part of the font file.helpviewer_keywords: ["BeginDownload","BeginDownload method [Direct Write]","BeginDownload method [Direct Write]","IDWriteRemoteFontFileStream interface","IDWriteRemoteFontFileStream interface [Direct Write]","BeginDownload method","IDWriteRemoteFontFileStream.BeginDownload","IDWriteRemoteFontFileStream::BeginDownload","directwrite.idwriteremotefontfilestream_begindownload","dwrite_3/IDWriteRemoteFontFileStream::BeginDownload"]
old-location: directwrite\idwriteremotefontfilestream_begindownload.htm
tech.root: DirectWrite
ms.assetid: A0EE8383-81A8-4974-B213-142704EFA210
ms.date: 12/05/2018
ms.keywords: BeginDownload, BeginDownload method [Direct Write], BeginDownload method [Direct Write],IDWriteRemoteFontFileStream interface, IDWriteRemoteFontFileStream interface [Direct Write],BeginDownload method, IDWriteRemoteFontFileStream.BeginDownload, IDWriteRemoteFontFileStream::BeginDownload, directwrite.idwriteremotefontfilestream_begindownload, dwrite_3/IDWriteRemoteFontFileStream::BeginDownload
f1_keywords:
- dwrite_3/IDWriteRemoteFontFileStream.BeginDownload
dev_langs:
- c++
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
- IDWriteRemoteFontFileStream.BeginDownload
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteRemoteFontFileStream::BeginDownload


## -description


Begins downloading all or part of the font file.


## -parameters




### -param downloadOperationID [in]

Type: <b>UUID</b>


### -param fileFragments [in]

Type: <b><a href="/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_file_fragment">DWRITE_FILE_FRAGMENT</a></b>

Array of structures, each specifying a byte range to download.


### -param fragmentCount

Type: <b>UINT32</b>

Number of elements in the fileFragments array. This can be zero to just download file information, such as the size.


### -param asyncResult

Type: <b>_COM_Outptr_result_maybenull_</b>

Receives an object that can be used to wait for the asynchronous download to complete and to get the download result upon 
          completion. The result may be NULL if the download completes synchronously. For example, this can happen if method determines that the requested data
          is already local.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -see-also




<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream">IDWriteRemoteFontFileStream</a>
 

 

