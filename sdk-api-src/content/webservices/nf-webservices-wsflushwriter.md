---
UID: NF:webservices.WsFlushWriter
title: WsFlushWriter function (webservices.h)
author: windows-sdk-content
description: Instructs the writer to invoke the callbackspecified in WS_XML_WRITER_STREAM_OUTPUT if sufficient data has been buffered.
old-location: wsw\wsflushwriter.htm
tech.root: wsw
ms.assetid: ba631942-d5a0-4d93-9899-c3f0ebd4aae5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WsFlushWriter, WsFlushWriter function [Web Services for Windows], webservices/WsFlushWriter, wsw.wsflushwriter
ms.topic: function
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsFlushWriter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsFlushWriter function


## -description


Instructs the writer to invoke the <a href="https://msdn.microsoft.com/8d106ac2-226d-4e0c-8f14-8d3e17f15548">callback</a>specified in <a href="https://msdn.microsoft.com/en-us/library/Dd323585(v=VS.85).aspx">WS_XML_WRITER_STREAM_OUTPUT</a> if sufficient data has been buffered.
      


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
      

This function is a no-op if the writer is using <a href="https://msdn.microsoft.com/en-us/library/Dd323575(v=VS.85).aspx">WS_XML_WRITER_BUFFER_OUTPUT</a>.
      

If <a href="https://msdn.microsoft.com/da23f5e6-504c-4e93-9190-7d8c41efc0da">WsWriteStartElement</a> has been called, but the element has not been committed (see <b>WsWriteStartElement</b>)
        then this element will not be flushed.
      

If this function is called when using <a href="https://msdn.microsoft.com/en-us/library/Dd323578(v=VS.85).aspx">WS_XML_WRITER_MTOM_ENCODING</a> and there are
        no open elements on the writer, then the supporting MIME parts will be generated and emitted.  Once this
        occurs, any API that attempts to write further to the XML document will return <b>WS_E_INVALID_OPERATION</b>.
      (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.)



