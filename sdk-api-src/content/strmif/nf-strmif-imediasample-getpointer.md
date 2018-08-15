---
UID: NF:strmif.IMediaSample.GetPointer
title: IMediaSample::GetPointer
author: windows-sdk-content
description: The GetPointer method retrieves a read/write pointer to the media sample's buffer.
old-location: dshow\imediasample_getpointer.htm
old-project: DirectShow
ms.assetid: a3c69dfb-6ee4-401b-8dcb-4e42a8cd8156
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: GetPointer, GetPointer method [DirectShow], GetPointer method [DirectShow],IMediaSample interface, IMediaSample interface [DirectShow],GetPointer method, IMediaSample.GetPointer, IMediaSample::GetPointer, IMediaSampleGetPointer, dshow.imediasample_getpointer, strmif/IMediaSample::GetPointer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.redist: 
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMediaSample.GetPointer
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IMediaSample::GetPointer


## -description



The <code>GetPointer</code> method retrieves a read/write pointer to the media sample's buffer.




## -parameters




### -param ppBuffer [out]

Receives a pointer to the buffer.


## -returns



Returns S_OK if successful, or an <b>HRESULT</b> value indicating the cause of the error.




## -remarks



The buffer memory is owned by the media sample object, and is automatically released when the media sample is destroyed. The caller should not free or reallocate the buffer.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/883e5e3b-db91-4806-96cc-c6f8cddfcca6">IMediaSample Interface</a>
 

 

