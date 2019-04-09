---
UID: NF:mediaobj.IMediaBuffer.SetLength
title: IMediaBuffer::SetLength (mediaobj.h)
author: windows-sdk-content
description: The SetLength method specifies the length of the data currently in the buffer.
old-location: dshow\imediabuffer_setlength.htm
tech.root: DirectShow
ms.assetid: 06cfbfd3-d196-4adb-a6b3-9b5f88bc03a6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMediaBuffer interface [DirectShow],SetLength method, IMediaBuffer.SetLength, IMediaBuffer::SetLength, IMediaBufferSetLength, SetLength, SetLength method [DirectShow], SetLength method [DirectShow],IMediaBuffer interface, dshow.imediabuffer_setlength, mediaobj/IMediaBuffer::SetLength
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
 - IMediaBuffer.SetLength
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaBuffer::SetLength


## -description



The <code>SetLength</code> method specifies the length of the data currently in the buffer.




## -parameters




### -param cbLength

Size of the data, in bytes. The value must not exceed the buffer's maximum size. Call the <a href="https://msdn.microsoft.com/en-us/library/Dd390168(v=VS.85).aspx">IMediaBuffer::GetMaxLength</a> method to obtain the maximum size.


## -returns



Returns S_OK if successful. Otherwise, returns an <b>HRESULT</b> value indicating the cause of the error.




## -remarks



This method sets the size of the valid data currently in the buffer, not the buffer's allocated size.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd390166(v=VS.85).aspx">IMediaBuffer Interface</a>



<a href="https://msdn.microsoft.com/bde7cef8-f43e-4a11-8b77-fed5585d390a">Implementing IMediaBuffer</a>
 

 

