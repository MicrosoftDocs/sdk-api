---
UID: NF:webservices.WsFillBody
title: WsFillBody function
author: windows-sdk-content
description: Ensures that there are a sufficient number of bytes available in a message for reading.
old-location: wsw\wsfillbody.htm
tech.root: wsw
ms.assetid: fe70338d-d2bf-4126-96b2-30ef6ebfa74d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WsFillBody, WsFillBody function [Web Services for Windows], webservices/WsFillBody, wsw.wsfillbody
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
 - WsFillBody
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsFillBody function


## -description


Ensures that there are a sufficient
                number of bytes available in a message for reading.  It is up to the application
                to specify the number of bytes sufficient to contain the
                next XML construct to read.
            
            
                <div class="alert"><b>Note</b>  This function is called before using <a href="https://msdn.microsoft.com/43ceeb1e-aeb2-4482-90f0-d7f6013b239f">WsReadBody</a> or the XML Readerof the message to read the message body.  </div>
<div> </div>


This function is a shortcut for calling <a href="https://msdn.microsoft.com/1f4138a2-acc5-4f1d-8e35-544859d2fa49">WsFillReader</a> for
                the  XML Reader being used to write the message.  Calling
                <b>WsFillReader</b> directly is equivalent to calling this function.
            


## -parameters




### -param message [in]

A pointer to the <a href="https://msdn.microsoft.com/22cc39a9-a3a7-4b4d-bdee-0ccac5dc03ee">WS_MESSAGE</a> structure intended for "filling".
        


### -param minSize [in]

The minimum number of bytes that the message should have buffered.
                    If the current byte count buffered is equal to or greater than the value of <i>minSize</i> the function does nothing.
                

<div class="alert"><b>Note</b>  The value of  <i>minSize</i> represents the size of the encoded form of the XML that is expected.  This can vary by encoding and also how the actual XML is structured.
                    Typical use of this function is to select an expected upper bound byte count for  encoding or XML structure to ensure that the expected
                    data is read.
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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Start of message was received successfully.
                

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



This function is typically used when writing the message body with streamed mode set to  
                <a href="https://msdn.microsoft.com/6153bef6-f37f-4bc6-b1c5-5fbedd6bd234">WS_STREAMED_OUTPUT_TRANSFER_MODE</a>, or when using an
                XML Reader in streamed mode.
            

This function is a "no-op" when writing the message body and <a href="https://msdn.microsoft.com/6153bef6-f37f-4bc6-b1c5-5fbedd6bd234">WS_STREAMED_OUTPUT_TRANSFER_MODE</a> is not set, or with an
                XML Reader's mode set to <a href="https://msdn.microsoft.com/86277c29-d42f-4b6a-ba33-b836bef284e7">WS_XML_READER_BUFFER_INPUT</a>.
            



