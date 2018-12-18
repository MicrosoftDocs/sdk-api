---
UID: NF:amstream.IAMMultiMediaStream.Render
title: IAMMultiMediaStream::Render
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The Render method renders the current filter graph.
old-location: dshow\iammultimediastream_render.htm
tech.root: DirectShow
ms.assetid: 09866cf0-650d-4d8e-81d4-6a568709c027
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAMMultiMediaStream interface [DirectShow],Render method, IAMMultiMediaStream.Render, IAMMultiMediaStream::Render, IAMMultiMediaStreamRender, Render, Render method [DirectShow], Render method [DirectShow],IAMMultiMediaStream interface, amstream/IAMMultiMediaStream::Render, dshow.iammultimediastream_render
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
 - IAMMultiMediaStream.Render
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMMultiMediaStream::Render


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>Render</code> method renders the current filter graph.




## -parameters




### -param dwFlags [in]

Value that specifies how the filter graph renders the current multimedia stream. This value currently must be AMMSF_NOCLOCK.


## -returns



Returns S_OK if successful or E_INVALIDARG if the <i>dwFlags</i> parameter is invalid.




## -remarks



This method renders each of the source streams for a stream of type STREAMTYPE_WRITE. This can be called several times, for instance, each time a source stream is added, the stream is not set into running mode. Use the <a href="https://msdn.microsoft.com/en-us/library/Dd390335(v=VS.85).aspx">IMultiMediaStream::SetState</a> method to set the stream into running mode after calling this method.

The AMMSF_RENDERALLSTREAMS flag will create default rendering streams for video and audio if they do not exist.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd319688(v=VS.85).aspx">IAMMultiMediaStream Interface</a>
 

 

