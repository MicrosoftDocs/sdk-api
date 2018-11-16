---
UID: NF:ddstream.IDirectDrawMediaStream.SetDirectDraw
title: IDirectDrawMediaStream::SetDirectDraw
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. Sets the current media stream's DirectDraw object.
old-location: dshow\idirectdrawmediastream_setdirectdraw.htm
tech.root: DirectShow
ms.assetid: ffa425c5-5f81-4963-bf23-2139d8b245b3
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IDirectDrawMediaStream interface [DirectShow],SetDirectDraw method, IDirectDrawMediaStream.SetDirectDraw, IDirectDrawMediaStream::SetDirectDraw, IDirectDrawMediaStreamSetDirectDraw, SetDirectDraw, SetDirectDraw method [DirectShow], SetDirectDraw method [DirectShow],IDirectDrawMediaStream interface, ddstream/IDirectDrawMediaStream::SetDirectDraw, dshow.idirectdrawmediastream_setdirectdraw
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ddstream.h
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
 - ddstream.h
api_name:
 - IDirectDrawMediaStream.SetDirectDraw
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- ddstream.h
: 
- IDirectDrawMediaStream.SetDirectDraw
: 
---

# IDirectDrawMediaStream::SetDirectDraw


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Sets the current media stream's DirectDraw object.




## -parameters




### -param pDirectDraw [in]

Pointer to an <b>IDirectDraw</b> interface that contains the media stream's new DirectDraw object.


## -returns



Returns S_OK if successful or E_POINTER if the pointer is invalid.




## -remarks



This method fails if the current stream already has allocated samples and its DirectDraw object differs from the specified one. It will always succeed if the specified DirectDraw object matches the stream's current object.

If this stream has no allocated samples, you can set <i>pDirectDraw</i> to <b>NULL</b>. This forces the stream to release its reference to the current DirectDraw object.




## -see-also




<a href="https://msdn.microsoft.com/858af0c3-9e22-45d8-ab08-307eb39a8977">IDirectDrawMediaStream Interface</a>
 

 

