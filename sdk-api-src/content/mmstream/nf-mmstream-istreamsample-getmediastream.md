---
UID: NF:mmstream.IStreamSample.GetMediaStream
title: IStreamSample::GetMediaStream
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. Retrieves a pointer to the media stream object that created the current sample.
old-location: dshow\istreamsample_getmediastream.htm
tech.root: DirectShow
ms.assetid: dfc38480-7b8d-42ad-937b-dd39384796c9
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: GetMediaStream, GetMediaStream method [DirectShow], GetMediaStream method [DirectShow],IStreamSample interface, IStreamSample interface [DirectShow],GetMediaStream method, IStreamSample.GetMediaStream, IStreamSample::GetMediaStream, IStreamSampleGetMediaStream, dshow.istreamsample_getmediastream, mmstream/IStreamSample::GetMediaStream
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
 - IStreamSample.GetMediaStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStreamSample::GetMediaStream


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Retrieves a pointer to the media stream object that created the current sample.




## -parameters




### -param ppMediaStream [in]

Address of a pointer to an <a href="https://msdn.microsoft.com/97f5dfdc-5941-4b58-a618-1c7e9f6665e1">IMediaStream</a> interface that will point to the media stream that created the current sample.


## -returns



Returns S_OK if successful or E_POINTER if <i>ppMediaStream</i> is invalid.




## -remarks



If successful, this method increments the reference count of the media stream specified by <i>ppMediaStream</i>.




## -see-also




<a href="https://msdn.microsoft.com/57818d7d-3290-46f7-a3fd-8585cdd64ec3">IStreamSample Interface</a>
 

 

