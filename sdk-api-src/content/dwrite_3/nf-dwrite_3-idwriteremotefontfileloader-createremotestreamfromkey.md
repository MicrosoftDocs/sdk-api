---
UID: NF:dwrite_3.IDWriteRemoteFontFileLoader.CreateRemoteStreamFromKey
title: IDWriteRemoteFontFileLoader::CreateRemoteStreamFromKey
author: windows-sdk-content
description: Creates a remote font file stream object that encapsulates an open file resource and can be used to download remote file data.
old-location: directwrite\idwriteremotefontfileloader_createremotestreamfromkey.htm
tech.root: DirectWrite
ms.assetid: 434B7349-0FD3-492F-8973-600A0A0DFA7B
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateRemoteStreamFromKey, CreateRemoteStreamFromKey method [Direct Write], CreateRemoteStreamFromKey method [Direct Write],IDWriteRemoteFontFileLoader interface, IDWriteRemoteFontFileLoader interface [Direct Write],CreateRemoteStreamFromKey method, IDWriteRemoteFontFileLoader.CreateRemoteStreamFromKey, IDWriteRemoteFontFileLoader::CreateRemoteStreamFromKey, directwrite.idwriteremotefontfileloader_createremotestreamfromkey, dwrite_3/IDWriteRemoteFontFileLoader::CreateRemoteStreamFromKey
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
 - IDWriteRemoteFontFileLoader.CreateRemoteStreamFromKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Mt807699(v=VS.85).aspx">IDWriteRemoteFontFileStream</a>**</b>

Pointer to the newly created font file stream.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -remarks



Unlike <a href="https://msdn.microsoft.com/1c0a7c7b-8201-45c5-ac46-20f0df034ccd">CreateStreamFromKey</a>, this method can be used to create a stream for a remote file. 
        If the file is remote, the client must call <a href="https://msdn.microsoft.com/en-us/library/Mt807700(v=VS.85).aspx">IDWriteRemoteFontFileStream::BeginDownload</a> with an empty array 
        of file fragments before the stream can be used to get the file size or access data.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt807695(v=VS.85).aspx">IDWriteRemoteFontFileLoader</a>
 

 

