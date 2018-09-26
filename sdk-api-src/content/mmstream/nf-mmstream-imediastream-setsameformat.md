---
UID: NF:mmstream.IMediaStream.SetSameFormat
title: IMediaStream::SetSameFormat
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. Sets the media stream to the same format as a previous stream.
old-location: dshow\imediastream_setsameformat.htm
tech.root: DirectShow
ms.assetid: 6a228547-7187-4a7a-8850-2681e0ccb13e
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IMediaStream interface [DirectShow],SetSameFormat method, IMediaStream.SetSameFormat, IMediaStream::SetSameFormat, IMediaStreamSetSameFormat, SetSameFormat, SetSameFormat method [DirectShow], SetSameFormat method [DirectShow],IMediaStream interface, dshow.imediastream_setsameformat, mmstream/IMediaStream::SetSameFormat
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mmstream.h
api_name:
 - IMediaStream.SetSameFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaStream::SetSameFormat


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Sets the media stream to the same format as a previous stream.




## -parameters




### -param pStreamThatHasDesiredFormat [in]

Pointer to a media stream object that has the same format.


### -param dwFlags [in]

Reserved for flag data. Must be zero.


## -returns



Returns S_OK if successful or E_POINTER if one of the parameters is invalid.




## -see-also




<a href="https://msdn.microsoft.com/97f5dfdc-5941-4b58-a618-1c7e9f6665e1">IMediaStream Interface</a>
 

 

