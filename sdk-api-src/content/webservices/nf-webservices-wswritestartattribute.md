---
UID: NF:webservices.WsWriteStartAttribute
title: WsWriteStartAttribute function
author: windows-sdk-content
description: This operation starts writing an attribute to the current element.
old-location: wsw\wswritestartattribute.htm
tech.root: wsw
ms.assetid: 9fd1eed9-6d8b-4b2e-a7ad-54a7f584734f
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: WsWriteStartAttribute, WsWriteStartAttribute function [Web Services for Windows], webservices/WsWriteStartAttribute, wsw.wswritestartattribute
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
 - WsWriteStartAttribute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsWriteStartAttribute function


## -description


This operation starts writing an attribute to the current element.
      <a href="https://msdn.microsoft.com/da23f5e6-504c-4e93-9190-7d8c41efc0da">WsWriteStartElement</a> must be called before an attribute can be written.
      After the attribute has been started, the attribute value can be written
        using <a href="https://msdn.microsoft.com/e435058f-62b5-4ae9-800e-e022033a9664">WsWriteChars</a>, <a href="https://msdn.microsoft.com/1fa9ecfc-c791-459f-ae11-ffcdc82b7145">WsWriteBytes</a>, or <a href="https://msdn.microsoft.com/c7b9d014-89b5-4959-b49e-ee2cdeb41f7c">WsWriteValue</a>. The attribute must
        be completed using using <a href="https://msdn.microsoft.com/8747c484-19b3-46b2-beee-80b220011def">WsWriteEndAttribute</a>.
      


## -parameters




### -param writer [in]

A pointer to the <a href="https://msdn.microsoft.com/8f413e60-8a30-492c-8f2d-80be511fee11">WS_XML_WRITER</a> object to which the attribute is written.  The pointer must reference a valid <b>XML Writer</b> object.
                


### -param prefix [in, optional]

A WS_XML_STRING pointer to the prefix to use for the attribute.  If the value referenced by this parameter is <b>NULL</b> the Writer will choose a attribute.
        


### -param localName [in]

A WS_XML_STRING pointer to the local name used by the attribute.  It must be at least one character long.
        


### -param ns [in]

A WS_XML_STRING pointer to the namespace to be used for the attribute.
        
          If no prefix is specified the Writer may use a prefix in scope that is bound to the specified namespace or it
          may generate a prefix and include an XMLNS attribute.
        If a prefix is specified the Writer will use that prefix and may include an XMLNS attribute if needed to override
          an existing prefix in scope.
        


### -param singleQuote [in]

Determines whether to use a single or a double quote for the attribute value.
        <div class="alert"><b>Note</b>  With <a href="https://msdn.microsoft.com/b4485490-b5e1-406c-883c-a30bfa334316">WS_XML_WRITER_BINARY_ENCODING</a> the quote character is not preserved and this
          parameter has no effect.
        </div>
<div> </div>





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



If a <b>NULL</b> prefix is specified the writer will choose a prefix for the namespace.
      

To write an "xml:lang"  or "xml:space" attribute, specify "xml" for the prefix, "lang" or "space" for the localName,
        and "http://www.w3.org/XML/1998/namespace" for the namespace.
      

If writing the attribute causes <a href="https://msdn.microsoft.com/c919eb01-bd15-4583-afcf-e46ac2fc9c8c">WS_XML_WRITER_PROPERTY_MAX_ATTRIBUTES</a> to be exceeded
        then <b>WS_E_QUOTA_EXCEEDED</b> is returned.
      

If a non-empty prefix is specified with an empty namespace <b>WS_E_INVALID_FORMAT</b> is returned.
      (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.)



