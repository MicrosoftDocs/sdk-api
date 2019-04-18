---
UID: NF:strmif.IPin.EndOfStream
title: IPin::EndOfStream (strmif.h)
author: windows-sdk-content
description: The EndOfStream method notifies the pin that no additional data is expected, until a new run command is issued to the filter.
old-location: dshow\ipin_endofstream.htm
tech.root: DirectShow
ms.assetid: b0cca250-9603-4d58-8af5-5b272730e5fa
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EndOfStream, EndOfStream method [DirectShow], EndOfStream method [DirectShow],IPin interface, IPin interface [DirectShow],EndOfStream method, IPin.EndOfStream, IPin::EndOfStream, IPinEndOfStream, dshow.ipin_endofstream, strmif/IPin::EndOfStream
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
 - IPin.EndOfStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPin::EndOfStream


## -description



The <code>EndOfStream</code> method notifies the pin that no additional data is expected, until a new run command is issued to the filter.



Applications should not call this method. This method is called by other filters to signal the end of the stream.


## -parameters






## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The pin is an output pin.

</td>
</tr>
</table>
 




## -remarks



Call this method only on input pins. Output pins return E_UNEXPECTED.

This method sends an end-of-stream notification to the pin. The pin delivers the notification downstream. It must serialize end-of-stream notifications with <a href="https://msdn.microsoft.com/7cc1e57a-a18a-4ea4-9669-0be3fb140d40">IMemInputPin::Receive</a> calls. If the pin queues media samples for delivery, it should queue end-of-stream notifications as well. The <a href="https://msdn.microsoft.com/15563666-5f35-46a0-ad12-215979c9d9c1">IPin::BeginFlush</a> method flushes any queued end-of-stream notifications.




## -see-also




<a href="https://msdn.microsoft.com/3fcfd874-39bc-42d2-9fc9-2d8945ffa8e3">Data Flow in the Filter Graph</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin Interface</a>
 

 

