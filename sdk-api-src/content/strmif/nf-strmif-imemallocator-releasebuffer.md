---
UID: NF:strmif.IMemAllocator.ReleaseBuffer
title: IMemAllocator::ReleaseBuffer
author: windows-sdk-content
description: The ReleaseBuffer method releases a media sample.
old-location: dshow\imemallocator_releasebuffer.htm
tech.root: DirectShow
ms.assetid: 96e02a28-af92-41a7-8251-c4ab15190651
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IMemAllocator interface [DirectShow],ReleaseBuffer method, IMemAllocator.ReleaseBuffer, IMemAllocator::ReleaseBuffer, IMemAllocatorReleaseBuffer, ReleaseBuffer, ReleaseBuffer method [DirectShow], ReleaseBuffer method [DirectShow],IMemAllocator interface, dshow.imemallocator_releasebuffer, strmif/IMemAllocator::ReleaseBuffer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMemAllocator.ReleaseBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMemAllocator::ReleaseBuffer


## -description



The <code>ReleaseBuffer</code> method releases a media sample.




## -parameters




### -param pBuffer [in]

Pointer to the media sample's <a href="https://msdn.microsoft.com/883e5e3b-db91-4806-96cc-c6f8cddfcca6">IMediaSample</a> interface.


## -returns



Returns S_OK if successful, or an <b>HRESULT</b> value indicating the cause of the error.




## -remarks



When a media sample's reference count reaches zero, it calls this method with itself as the <i>pBuffer</i> parameter. This method releases the sample back to the allocator's list of available samples.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/77a161c4-706c-4270-a343-9e16c03cd590">IMemAllocator Interface</a>
 

 

