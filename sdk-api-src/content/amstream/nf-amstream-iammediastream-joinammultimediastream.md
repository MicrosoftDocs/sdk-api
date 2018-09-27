---
UID: NF:amstream.IAMMediaStream.JoinAMMultiMediaStream
title: IAMMediaStream::JoinAMMultiMediaStream
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The IAMMultiMediaStream::AddMediaStream method calls this method, which adds the specified media stream to the current multimedia stream.
old-location: dshow\iammediastream_joinammultimediastream.htm
tech.root: DirectShow
ms.assetid: c842b841-a4dc-47c8-8186-347aff2c4ac3
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IAMMediaStream interface [DirectShow],JoinAMMultiMediaStream method, IAMMediaStream.JoinAMMultiMediaStream, IAMMediaStream::JoinAMMultiMediaStream, IAMMediaStreamJoinAMMultiMediaStream, JoinAMMultiMediaStream, JoinAMMultiMediaStream method [DirectShow], JoinAMMultiMediaStream method [DirectShow],IAMMediaStream interface, amstream/IAMMediaStream::JoinAMMultiMediaStream, dshow.iammediastream_joinammultimediastream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: amstream.h
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
 - amstream.h
api_name:
 - IAMMediaStream.JoinAMMultiMediaStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMMediaStream::JoinAMMultiMediaStream


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <a href="https://msdn.microsoft.com/3ccfb776-6a4e-48da-857d-6693cf916c40">IAMMultiMediaStream::AddMediaStream</a> method calls this method, which adds the specified media stream to the current multimedia stream.




## -parameters




### -param pAMMultiMediaStream [in]

Pointer to the <a href="https://msdn.microsoft.com/2f604156-68ef-4770-9929-6dbfd46c4d6d">IAMMultiMediaStream</a> object to add the current media stream to.


## -returns



Returns S_OK if successful or MS_E_SAMPLEALLOC if the media stream already has allocated stream samples.




## -remarks



Don't increment the reference count of the supplied multimedia stream because it is already accounted for when created.

Applications should not call this method.




## -see-also




<a href="https://msdn.microsoft.com/14185e7d-d08d-4fd8-a255-075eaf12a708">IAMMediaStream Interface</a>
 

 

