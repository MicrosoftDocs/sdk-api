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

This method sends an end-of-stream notification to the pin. The pin delivers the notification downstream. It must serialize end-of-stream notifications with <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imeminputpin-receive">IMemInputPin::Receive</a> calls. If the pin queues media samples for delivery, it should queue end-of-stream notifications as well. The <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipin-beginflush">IPin::BeginFlush</a> method flushes any queued end-of-stream notifications.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/data-flow-in-the-filter-graph">Data Flow in the Filter Graph</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ipin">IPin Interface</a>
 

 

