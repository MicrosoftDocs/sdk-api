---
UID: NF:webservices.WsWriteBytes
title: WsWriteBytes function
author: windows-sdk-content
description: Writes bytes to the writer in a format optimized for the encoding. When writing in a text encoding, it will emit the bytes encoded in base64. When writing to a binary format, it will emit the bytes directly.
old-location: wsw\wswritebytes.htm
tech.root: wsw
ms.assetid: 1fa9ecfc-c791-459f-ae11-ffcdc82b7145
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WsWriteBytes, WsWriteBytes function [Web Services for Windows], webservices/WsWriteBytes, wsw.wswritebytes
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
 - WsWriteBytes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsWriteBytes function


## -description


Writes bytes to the writer in a format optimized for the encoding.  When writing
         in a text encoding, it will emit the bytes encoded in base64.  When writing to 
         a binary format, it will emit the bytes directly.
      


## -parameters




### -param writer [in]

The writer to which the bytes will be written.
        


### -param bytes

The bytes to write to the document.
        


### -param byteCount [in]

The number bytes to write to the document.
        


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
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The operation is not allowed due to the current state of the object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_QUOTA_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
A quota was exceeded.

</td>
</tr>
</table>
 




## -remarks



<b>WsWriteBytes</b> may be called more than once between <a href="https://msdn.microsoft.com/9fd1eed9-6d8b-4b2e-a7ad-54a7f584734f">WsWriteStartAttribute</a> and <a href="https://msdn.microsoft.com/8747c484-19b3-46b2-beee-80b220011def">WsWriteEndAttribute</a>.  It may
        not be combined with <a href="https://msdn.microsoft.com/e435058f-62b5-4ae9-800e-e022033a9664">WsWriteChars</a>, <a href="https://msdn.microsoft.com/53cdaf22-21ed-4e5a-8034-d5a4725b9da3">WsWriteCharsUtf8</a>, <a href="https://msdn.microsoft.com/c7b9d014-89b5-4959-b49e-ee2cdeb41f7c">WsWriteValue</a> or <a href="https://msdn.microsoft.com/a4ffc05e-d04a-4cc3-bdb6-71b2090bc32f">WsWriteText</a>when writing an attribute.
      

For the <a href="https://msdn.microsoft.com/18236818-492f-4906-9e7d-6ca03ef28d36">WS_XML_WRITER_MTOM_ENCODING</a>, if the byteCount exceeds the maxInlineByteCount specified
        during <a href="https://msdn.microsoft.com/f0b47817-0ad1-408c-a6da-9a7b0fb2e34b">WsSetOutput</a> then the bytes will be buffered and  placed in their own MIME part.  Otherwise
        the bytes are encoded in base64 and placed directly in the document.
      

For the <a href="https://msdn.microsoft.com/18236818-492f-4906-9e7d-6ca03ef28d36">WS_XML_WRITER_MTOM_ENCODING</a>, if the element containing the bytes has an attribute with
        the name 'contentType' and the namespace 'http://www.w3.org/2004/11/xmlmime', then the value of the attribute
        will be reflected in the content type header for the MIME part as described in 
        XML-binary Optimized Packaging.
      



