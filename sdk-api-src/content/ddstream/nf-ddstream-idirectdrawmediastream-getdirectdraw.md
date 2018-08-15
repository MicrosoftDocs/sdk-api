---
UID: NF:ddstream.IDirectDrawMediaStream.GetDirectDraw
title: IDirectDrawMediaStream::GetDirectDraw
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. Retrieves a pointer to the DirectDraw object used by the current media stream.
old-location: dshow\idirectdrawmediastream_getdirectdraw.htm
old-project: DirectShow
ms.assetid: 44c505fe-70d9-49bd-9135-8a6dc2c72e98
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: GetDirectDraw, GetDirectDraw method [DirectShow], GetDirectDraw method [DirectShow],IDirectDrawMediaStream interface, IDirectDrawMediaStream interface [DirectShow],GetDirectDraw method, IDirectDrawMediaStream.GetDirectDraw, IDirectDrawMediaStream::GetDirectDraw, IDirectDrawMediaStreamGetDirectDraw, ddstream/IDirectDrawMediaStream::GetDirectDraw, dshow.idirectdrawmediastream_getdirectdraw
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ddstream.h
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
req.typenames: VIDEOMEMORYINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ddstream.h
api_name:
 - IDirectDrawMediaStream.GetDirectDraw
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectDrawMediaStream::GetDirectDraw


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Retrieves a pointer to the DirectDraw object used by the current media stream.




## -parameters




### -param ppDirectDraw [out]

Address of a pointer to an <b>IDirectDraw</b> interface that will contain the current media stream's associated DirectDraw object.


## -returns



Returns S_OK if successful or E_POINTER if the parameter is invalid.




## -remarks



If you haven't initialized the stream yet, the retrieved pointer will be <b>NULL</b> and the method will return S_OK. If you have initialized the stream, this method increments the retrieved pointer's reference count.




## -see-also




<a href="https://msdn.microsoft.com/858af0c3-9e22-45d8-ab08-307eb39a8977">IDirectDrawMediaStream Interface</a>
 

 

