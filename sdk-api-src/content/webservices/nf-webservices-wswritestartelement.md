---
UID: NF:webservices.WsWriteStartElement
title: WsWriteStartElement function
author: windows-sdk-content
description: Writes a start element to the writer.
old-location: wsw\wswritestartelement.htm
tech.root: wsw
ms.assetid: da23f5e6-504c-4e93-9190-7d8c41efc0da
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WsWriteStartElement, WsWriteStartElement function [Web Services for Windows], webservices/WsWriteStartElement, wsw.wswritestartelement
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
 - WsWriteStartElement
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsWriteStartElement function


## -description


Writes a start element to the writer.
      

After calling this function <a href="https://msdn.microsoft.com/9fd1eed9-6d8b-4b2e-a7ad-54a7f584734f">WsWriteStartAttribute</a> or <a href="https://msdn.microsoft.com/17d73228-ea3b-4212-b9f7-7dcfdd6043a3">WsWriteXmlnsAttribute</a>can be called to write additional attributes to the element.
      The element is not committed to the writer until <a href="https://msdn.microsoft.com/cfb23857-bc51-4467-9aeb-6ce8810ae1b0">WsWriteEndElement</a> or some other function  that 
        writes content is called.
      


## -parameters




### -param writer [in]

A pointer to the <a href="https://msdn.microsoft.com/8f413e60-8a30-492c-8f2d-80be511fee11">WS_XML_WRITER</a> object to which the start element is written.  The pointer must reference a valid <b>XML Writer</b> object.
                


### -param prefix [in, optional]

A WS_XML_STRING pointer to the prefix to use for the start element.  If the value referenced by this parameter is <b>NULL</b> the Writer will choose a attribute.
        


### -param localName [in]

A WS_XML_STRING pointer to the local name used by the start element.  It must be at least one character long.
        


### -param ns [in]

A WS_XML_STRING pointer to the namespace to be used for the start element.
        
          If no prefix is specified the Writer may use a prefix in scope that is bound to the specified namespace or it
          may generate a prefix and include an XMLNS attribute.
        If a prefix is specified the Writer will use that prefix and may include an XMLNS attribute if needed to override
          an existing prefix in scope.
        


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
<dt><b>WS_E_QUOTA_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
A quota was exceeded.

</td>
</tr>
</table>
 




## -remarks



If the underlying encoding supports empty elements and the element has no content an empty element is written.
      

If a non-empty prefix is specified with an empty namespace <b>WS_E_INVALID_FORMAT</b> is returned.
      

If writing the start element causes <b>WS_XML_WRITER_PROPERTY_MAX_DEPTH</b> to be exceeded
        <b>WS_E_QUOTA_EXCEEDED</b> is returned.
       (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.)

When using <a href="https://msdn.microsoft.com/18236818-492f-4906-9e7d-6ca03ef28d36">WS_XML_WRITER_MTOM_ENCODING</a> it is an error to attempt to write an element with the
        localName "Include" from the namespace"http://www.w3.org/2004/08/xop/include".
      


<a href="https://msdn.microsoft.com/9fd1eed9-6d8b-4b2e-a7ad-54a7f584734f">WsWriteStartAttribute</a> can also be used to add an attribute to an element when the writer is
        positioned on an element using <a href="https://msdn.microsoft.com/f8eace53-9fa5-466a-8894-3c8b8fe049e3">WsMoveWriter</a> or <a href="https://msdn.microsoft.com/1d23bda1-d1da-44d4-9a9d-258bba200b29">WsSetWriterPosition</a>.
      



