---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# WsFlushWriter function


## -description



        Instructs the writer to invoke the <a href="https://msdn.microsoft.com/8d106ac2-226d-4e0c-8f14-8d3e17f15548">callback</a>
        specified in <a href="https://msdn.microsoft.com/8ee4ea59-5cdc-43bf-80c0-8f8632fee274">WS_XML_WRITER_STREAM_OUTPUT</a> if sufficient data has been buffered.
      


## -parameters




### -param writer [in]


          The writer to flush.
        


### -param minSize [in]


          Specifies the minimum number of bytes that must be buffered in order for the
          <a href="https://msdn.microsoft.com/8d106ac2-226d-4e0c-8f14-8d3e17f15548">callback</a> to be invoked. If fewer than this number of bytes
          are buffered, then the <b>callback</b> will not be invoked.  This can be
          used to minimize the number of i/o's that occur when writing small amounts of data.
        


          Zero should be specified to guarantee that the <a href="https://msdn.microsoft.com/8d106ac2-226d-4e0c-8f14-8d3e17f15548">callback</a> is invoked.
        


### -param asyncContext [in, optional]


          Information on how to invoke the function asynchronously, or <b>NULL</b> if invoking synchronously.
        


### -param error [in, optional]


          Specifies where additional error information should be stored if the function fails.
        


## -returns



This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">

One or more arguments are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_S_ASYNC</b></dt>
</dl>
</td>
<td width="60%">

          The asynchronous operation is still pending.
        

</td>
</tr>
</table>
 




## -remarks




        The writer buffers all data until <b>WsFlushWriter</b> is called.
      


        If necessary, the <b>WsFlushWriter</b> should be called before <a href="https://msdn.microsoft.com/eb1eb835-838a-41e4-9e7d-c5c805237f65">WsFreeWriter</a> to guarantee all data is emitted.
      


        By specifying a <a href="https://msdn.microsoft.com/3c9ffbef-2f5b-42b0-96b1-f17f0ab98ca4">WS_ASYNC_CONTEXT</a> the buffered data will be written asynchronously.
      


        This function is a no-op if the writer is using <a href="https://msdn.microsoft.com/46c0595c-9aa5-47cf-931a-8dc35e265fa0">WS_XML_WRITER_BUFFER_OUTPUT</a>.
      


        If <a href="https://msdn.microsoft.com/da23f5e6-504c-4e93-9190-7d8c41efc0da">WsWriteStartElement</a> has been called, but the element has not been committed (see <b>WsWriteStartElement</b>)
        then this element will not be flushed.
      


        If this function is called when using <a href="https://msdn.microsoft.com/18236818-492f-4906-9e7d-6ca03ef28d36">WS_XML_WRITER_MTOM_ENCODING</a> and there are
        no open elements on the writer, then the supporting MIME parts will be generated and emitted.  Once this
        occurs, any API that attempts to write further to the XML document will return <b>WS_E_INVALID_OPERATION</b>.
      (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.)



