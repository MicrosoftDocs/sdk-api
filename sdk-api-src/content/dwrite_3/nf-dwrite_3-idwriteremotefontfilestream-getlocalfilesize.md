---
UID: NF:dwrite_3.IDWriteRemoteFontFileStream.GetLocalFileSize
title: IDWriteRemoteFontFileStream::GetLocalFileSize
author: windows-sdk-content
description: GetLocalFileSize returns the number of bytes of the font file that are currently local, which should always be less than or equal to the full file size returned by GetFileSize.
old-location: directwrite\idwriteremotefontfilestream_getlocalfilesize.htm
tech.root: DirectWrite
ms.assetid: 06FB14D5-19F6-48D3-AEA9-3D622219EF2A
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetLocalFileSize, GetLocalFileSize method [Direct Write], GetLocalFileSize method [Direct Write],IDWriteRemoteFontFileStream interface, IDWriteRemoteFontFileStream interface [Direct Write],GetLocalFileSize method, IDWriteRemoteFontFileStream.GetLocalFileSize, IDWriteRemoteFontFileStream::GetLocalFileSize, directwrite.idwriteremotefontfilestream_getlocalfilesize, dwrite_3/IDWriteRemoteFontFileStream::GetLocalFileSize
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
 - IDWriteRemoteFontFileStream.GetLocalFileSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteRemoteFontFileStream::GetLocalFileSize


## -description


GetLocalFileSize returns the number of bytes of the font file that are currently local, which should always be less than or equal to the full
          file size returned by <a href="https://msdn.microsoft.com/52186ddb-ea08-4615-a3df-35ea7288270c">GetFileSize</a>. 
         If the locality is remote, the return value is zero. If the file is fully local, the return value must be the
          same as <a href="https://msdn.microsoft.com/52186ddb-ea08-4615-a3df-35ea7288270c">GetFileSize</a>.
      


## -parameters




### -param localFileSize [out]

Type: <b>UINT64*</b>

Receives the local size of the file.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -see-also




<a href="https://msdn.microsoft.com/2CC73CE0-162A-4808-ACB6-A9599FD4D09F">IDWriteRemoteFontFileStream</a>
 

 

