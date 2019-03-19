---
UID: NF:mediaobj.IMediaBuffer.GetMaxLength
title: IMediaBuffer::GetMaxLength (mediaobj.h)
author: windows-sdk-content
description: The GetMaxLength method retrieves the maximum number of bytes this buffer can hold.
old-location: dshow\imediabuffer_getmaxlength.htm
tech.root: DirectShow
ms.assetid: 9e312d3b-4994-4493-861c-cc0f6f112362
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetMaxLength, GetMaxLength method [DirectShow], GetMaxLength method [DirectShow],IMediaBuffer interface, IMediaBuffer interface [DirectShow],GetMaxLength method, IMediaBuffer.GetMaxLength, IMediaBuffer::GetMaxLength, IMediaBufferGetMaxLength, dshow.imediabuffer_getmaxlength, mediaobj/IMediaBuffer::GetMaxLength
ms.topic: method
req.header: mediaobj.h
req.include-header: Dmo.h
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
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaBuffer.GetMaxLength
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaBuffer::GetMaxLength


## -description



The <code>GetMaxLength</code> method retrieves the maximum number of bytes this buffer can hold.




## -parameters




### -param pcbMaxLength [out]

Pointer to a variable that receives the buffer's maximum size, in bytes.


## -returns



Returns S_OK if successful. Otherwise, returns an <b>HRESULT</b> value indicating the cause of the error.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd390166(v=VS.85).aspx">IMediaBuffer Interface</a>



<a href="https://msdn.microsoft.com/bde7cef8-f43e-4a11-8b77-fed5585d390a">Implementing IMediaBuffer</a>
 

 

