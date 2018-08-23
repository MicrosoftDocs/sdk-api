---
UID: NF:dwrite_3.IDWriteRemoteFontFileLoader.CreateRemoteStreamFromKey
title: IDWriteRemoteFontFileLoader::CreateRemoteStreamFromKey
author: windows-sdk-content
description: Creates a remote font file stream object that encapsulates an open file resource and can be used to download remote file data.
old-location: directwrite\idwriteremotefontfileloader_createremotestreamfromkey.htm
old-project: DirectWrite
ms.assetid: 434B7349-0FD3-492F-8973-600A0A0DFA7B
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: CreateRemoteStreamFromKey, CreateRemoteStreamFromKey method [Direct Write], CreateRemoteStreamFromKey method [Direct Write],IDWriteRemoteFontFileLoader interface, IDWriteRemoteFontFileLoader interface [Direct Write],CreateRemoteStreamFromKey method, IDWriteRemoteFontFileLoader.CreateRemoteStreamFromKey, IDWriteRemoteFontFileLoader::CreateRemoteStreamFromKey, directwrite.idwriteremotefontfileloader_createremotestreamfromkey, dwrite_3/IDWriteRemoteFontFileLoader::CreateRemoteStreamFromKey
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dwrite_3.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dwrite.lib
 - Dwrite.dll
api_name:
 - IDWriteRemoteFontFileLoader.CreateRemoteStreamFromKey
product: Windows
targetos: Windows
req.lib: Dwrite.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDWriteRemoteFontFileLoader::CreateRemoteStreamFromKey


## -description


Creates a remote font file stream object that encapsulates an open file resource and can be used to download remote file data.


## -parameters




### -param fontFileReferenceKey [in]

Type: <b>void</b>

Font file reference key that uniquely identifies the font file resource within the scope of the font loader being used.


### -param fontFileReferenceKeySize

Type: <b>UINT32</b>

Size of font file reference key in bytes.


### -param fontFileStream [out]

Type: <b><a href="https://msdn.microsoft.com/2CC73CE0-162A-4808-ACB6-A9599FD4D09F">IDWriteRemoteFontFileStream</a>**</b>

Pointer to the newly created font file stream.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -remarks



Unlike <a href="https://msdn.microsoft.com/1c0a7c7b-8201-45c5-ac46-20f0df034ccd">CreateStreamFromKey</a>, this method can be used to create a stream for a remote file. 
        If the file is remote, the client must call <a href="https://msdn.microsoft.com/A0EE8383-81A8-4974-B213-142704EFA210">IDWriteRemoteFontFileStream::BeginDownload</a> with an empty array 
        of file fragments before the stream can be used to get the file size or access data.




## -see-also




<a href="https://msdn.microsoft.com/16CFF7ED-642A-48D8-8C72-3EC68B702E50">IDWriteRemoteFontFileLoader</a>
 

 

