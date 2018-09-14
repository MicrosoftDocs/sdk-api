---
UID: NF:webservices.WsWriteElement
title: WsWriteElement function
author: windows-sdk-content
description: Write a typed value as an XML element.
old-location: wsw\wswriteelement.htm
tech.root: wsw
ms.assetid: 5416d167-b832-4815-9826-6128f68dbc02
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: WsWriteElement, WsWriteElement function [Web Services for Windows], webservices/WsWriteElement, wsw.wswriteelement
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
 - WsWriteElement
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsWriteElement function


## -description


Write a typed value as an XML element.
            


## -parameters




### -param writer [in]

The writer to write the element to.
                


### -param elementDescription [in]

A pointer to a description of how to serialize the element.
                


### -param writeOption [in]

Information about how the value is allocated.
                    See <a href="https://msdn.microsoft.com/24a0ad2c-fcec-42c5-8f72-bea431b06d2e">WS_WRITE_OPTION</a> for more information.
                


### -param value

A pointer to the value to serialize.
                


### -param valueSize [in]

The size of the value being serialized, in bytes.
                

If the value is <b>NULL</b>, then the size should be 0.
                


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
</table>
 




## -remarks



This API writes the start element, the attributes, child elements / text, and the end element
                that corresponds to the specified value.
            

If the API fails, the state of input writer becomes undefined. The only APIs that may be used on the writer
        if this occurs are <a href="https://msdn.microsoft.com/f0b47817-0ad1-408c-a6da-9a7b0fb2e34b">WsSetOutput</a> and <a href="https://msdn.microsoft.com/b969700d-7145-45eb-ad4b-c6e643975709">WsSetOutputToBuffer</a> to return the writer to a usable state,
        or <a href="https://msdn.microsoft.com/eb1eb835-838a-41e4-9e7d-c5c805237f65">WsFreeWriter</a> to free the writer.
            



