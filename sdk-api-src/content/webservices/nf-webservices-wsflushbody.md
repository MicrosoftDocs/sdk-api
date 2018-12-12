---
UID: NF:webservices.WsFlushBody
title: WsFlushBody function
author: windows-sdk-content
description: Flushes all accumulated message body data that has been written.
old-location: wsw\wsflushbody.htm
tech.root: wsw
ms.assetid: f94c409b-94c0-4440-8587-74322777261f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WsFlushBody, WsFlushBody function [Web Services for Windows], webservices/WsFlushBody, wsw.wsflushbody
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - WsFlushBody
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsFlushBody function


## -description


Flushes all accumulated message body data that has been written.
            

When message uses <a href="https://msdn.microsoft.com/70ff43f5-6f1a-4bbb-aa39-6fb9476e6a37">WsWriteBody</a> or XML Writerthe data is accumulated in a buffer.   WsFlushBody subsequently performs the actual
                I/O.
            

WsFlushBody is typically used when  channel I/O is set to 
                <a href="https://msdn.microsoft.com/en-us/library/Dd323477(v=VS.85).aspx">WS_STREAMED_OUTPUT_TRANSFER_MODE</a>, or when using an 
                XML Writer  set to use <a href="https://msdn.microsoft.com/8ee4ea59-5cdc-43bf-80c0-8f8632fee274">WS_XML_WRITER_STREAM_OUTPUT</a>.
            


## -parameters




### -param message [in]

A pointer to the <a href="https://msdn.microsoft.com/22cc39a9-a3a7-4b4d-bdee-0ccac5dc03ee">WS_MESSAGE</a> structure containing the accumulated message body data.


### -param minSize [in]

Specifies the minimum number of bytes that must be present in the
                    message for the function to perform the data flush.  
                

<div class="alert"><b>Note</b>  If the message contains less
                    than <i>minSize</i> WSFlushBody terminates without doing the I/O flush. A larger value will ensure that no I/O will be done until
                    the larger value has been accumulated.  This is useful for ensuring
                    that larger chunks are used when doing I/O.
                And presuming that 
                    there is at least one byte of accumulated data a value of 0 in  <i>minSize</i> guarantees that it will be flushed.
                </div>
<div> </div>

### -param asyncContext [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/3c9ffbef-2f5b-42b0-96b1-f17f0ab98ca4">WS_ASYNC_CONTEXT</a> data structure with information about invoking the function asynchronously.  A <b>NULL</b> 
                 value indicates a request for synchronous operation.


### -param error [in, optional]

A  pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object where additional information about the error should be stored if the function fails.
                


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
<dt><b>WS_S_ASYNC</b></dt>
</dl>
</td>
<td width="60%">
The asynchronous operation is still pending.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The input data was not in the expected format or did not have the expected value.

</td>
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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Ran out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> Other Errors </b></dt>
</dl>
</td>
<td width="60%">
This function may return other errors not listed above.

</td>
</tr>
</table>
 




## -remarks



This function is a "no-op" when <a href="https://msdn.microsoft.com/en-us/library/Dd323477(v=VS.85).aspx">WS_STREAMED_OUTPUT_TRANSFER_MODE</a> is not set, or when using an
                XML Writer with <a href="https://msdn.microsoft.com/46c0595c-9aa5-47cf-931a-8dc35e265fa0">WS_XML_WRITER_BUFFER_OUTPUT</a> set.
      

This function is shortcut for calling <a href="https://msdn.microsoft.com/ba631942-d5a0-4d93-9899-c3f0ebd4aae5">WsFlushWriter</a> for 
                the XML Writer being used to write the message.  Calling 
                <b>WsFlushWriter</b> directly is equivalent to calling this function.
            



