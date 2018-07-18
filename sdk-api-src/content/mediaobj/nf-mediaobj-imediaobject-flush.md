---
UID: NF:mediaobj.IMediaObject.Flush
title: IMediaObject::Flush
author: windows-sdk-content
description: The Flush method flushes all internally buffered data.
old-location: dshow\imediaobject_flush.htm
old-project: DirectShow
ms.assetid: c80001b8-5648-430a-b565-e90486c48ac5
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: Flush, Flush method [DirectShow], Flush method [DirectShow],IMediaObject interface, IMediaObject interface [DirectShow],Flush method, IMediaObject.Flush, IMediaObject::Flush, IMediaObjectFlush, dshow.imediaobject_flush, mediaobj/IMediaObject::Flush
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaObject.Flush
product: Windows
targetos: Windows
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMediaObject::Flush


## -description



The <code>Flush</code> method flushes all internally buffered data.




## -parameters






## -returns



Returns S_OK if successful. Otherwise, returns an <b>HRESULT</b> value indicating the cause of the error.




## -remarks



The DMO performs the following actions when this method is called:

<ul>
<li>Releases any <a href="https://msdn.microsoft.com/74d72ca6-f899-43fc-bdea-5208d920f314">IMediaBuffer</a> references it holds.</li>
<li>Discards any values that specify the time stamp or sample length for a media buffer.</li>
<li>Reinitializes any internal states that depend on the contents of a media sample.</li>
</ul>
Media types, maximum latency, and locked state do not change.

When the method returns, every input stream accepts data. Output streams cannot produce any data until the application calls the <a href="https://msdn.microsoft.com/f52e9586-f65d-418f-8c1a-c97c0a81d253">IMediaObject::ProcessInput</a> method on at least one input stream.




## -see-also




<a href="https://msdn.microsoft.com/a3fd17aa-7df2-40f4-8f2c-45bae38e4c0b">IMediaObject Interface</a>
 

 

