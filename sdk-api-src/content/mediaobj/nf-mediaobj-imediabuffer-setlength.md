---
UID: NF:mediaobj.IMediaBuffer.SetLength
title: IMediaBuffer::SetLength
author: windows-driver-content
description: The SetLength method specifies the length of the data currently in the buffer.
old-location: dshow\imediabuffer_setlength.htm
old-project: DirectShow
ms.assetid: 06cfbfd3-d196-4adb-a6b3-9b5f88bc03a6
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IMediaBuffer interface [DirectShow],SetLength method, IMediaBuffer.SetLength, IMediaBuffer::SetLength, IMediaBufferSetLength, SetLength, SetLength method [DirectShow], SetLength method [DirectShow],IMediaBuffer interface, dshow.imediabuffer_setlength, mediaobj/IMediaBuffer::SetLength
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Dmoguids.lib
-	Dmoguids.dll
api_name:
-	IMediaBuffer.SetLength
product: Windows
targetos: Windows
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMediaBuffer::SetLength


## -description



The <code>SetLength</code> method specifies the length of the data currently in the buffer.




## -parameters




### -param cbLength

Size of the data, in bytes. The value must not exceed the buffer's maximum size. Call the <a href="https://msdn.microsoft.com/9e312d3b-4994-4493-861c-cc0f6f112362">IMediaBuffer::GetMaxLength</a> method to obtain the maximum size.


## -returns



Returns S_OK if successful. Otherwise, returns an <b>HRESULT</b> value indicating the cause of the error.




## -remarks



This method sets the size of the valid data currently in the buffer, not the buffer's allocated size.




## -see-also




<a href="https://msdn.microsoft.com/74d72ca6-f899-43fc-bdea-5208d920f314">IMediaBuffer Interface</a>



<a href="https://msdn.microsoft.com/bde7cef8-f43e-4a11-8b77-fed5585d390a">Implementing IMediaBuffer</a>
 

 

