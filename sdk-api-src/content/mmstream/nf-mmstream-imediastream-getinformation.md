---
UID: NF:mmstream.IMediaStream.GetInformation
title: IMediaStream::GetInformation
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. Retrieves the stream's purpose ID and media type.
old-location: dshow\imediastream_getinformation.htm
old-project: DirectShow
ms.assetid: e4ecae45-e2bf-44dd-8901-0892c02d708c
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetInformation, GetInformation method [DirectShow], GetInformation method [DirectShow],IMediaStream interface, IMediaStream interface [DirectShow],GetInformation method, IMediaStream.GetInformation, IMediaStream::GetInformation, IMediaStreamGetInformation, dshow.imediastream_getinformation, mmstream/IMediaStream::GetInformation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mmstream.h
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
tech.root: 
req.typenames: STREAM_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mmstream.h
api_name:
 - IMediaStream.GetInformation
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMediaStream::GetInformation


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Retrieves the stream's purpose ID and media type.




## -parameters




### -param pPurposeId [out]

Pointer to an <b>MSPID</b> value that will contain the stream's purpose ID (see <a href="https://msdn.microsoft.com/750a7992-e2ef-4149-b1c8-c5201f6af035">Multimedia Streaming Data Types</a>). If this parameter is <b>NULL</b> on entry, the method won't retrieve the purpose ID.


### -param pType [out]

Pointer to a <a href="https://msdn.microsoft.com/07ab5ded-28b8-4cac-b4da-76f07ad351ef">STREAM_TYPE</a> enumerated data type value that will contain the stream's media type. If this parameter is <b>NULL</b> on entry, the method won't retrieve the media type.


## -returns



Returns S_OK if successful or E_POINTER if one of the parameters is invalid.




## -remarks



The value retrieved in the <i>pPurposeId</i> parameter will usually be either MSPID_PrimaryVideo, which identifies the primary video stream, or MSPID_PrimaryAudio, which identifies the primary audio stream; however, you can define other values if necessary.




## -see-also




<a href="https://msdn.microsoft.com/97f5dfdc-5941-4b58-a618-1c7e9f6665e1">IMediaStream Interface</a>
 

 

