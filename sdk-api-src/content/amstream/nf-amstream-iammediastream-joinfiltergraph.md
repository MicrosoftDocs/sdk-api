---
UID: NF:amstream.IAMMediaStream.JoinFilterGraph
title: IAMMediaStream::JoinFilterGraph
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The JoinFilterGraph method connects a media stream filter to a filter graph.
old-location: dshow\iammediastream_joinfiltergraph.htm
tech.root: DirectShow
ms.assetid: b14e9be4-f292-4a71-b541-4fda2640591d
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IAMMediaStream interface [DirectShow],JoinFilterGraph method, IAMMediaStream.JoinFilterGraph, IAMMediaStream::JoinFilterGraph, IAMMediaStreamJoinFilterGraph, JoinFilterGraph, JoinFilterGraph method [DirectShow], JoinFilterGraph method [DirectShow],IAMMediaStream interface, amstream/IAMMediaStream::JoinFilterGraph, dshow.iammediastream_joinfiltergraph
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
 - IAMMediaStream.JoinFilterGraph
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- amstream.h
: 
- IAMMediaStream.JoinFilterGraph
: 
---

# IAMMediaStream::JoinFilterGraph


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>JoinFilterGraph</code> method connects a media stream filter to a filter graph.




## -parameters




### -param pFilterGraph [in]

Pointer to the current media stream filter to add to the specified filter graph.


## -returns



Returns S_OK if successful or E_POINTER if <i>pGraph</i> is <b>NULL</b>.




## -remarks



Don't increment the reference count of the specified filter graph.

Applications should not call this method.




## -see-also




<a href="https://msdn.microsoft.com/14185e7d-d08d-4fd8-a255-075eaf12a708">IAMMediaStream Interface</a>
 

 

