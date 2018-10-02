---
UID: NF:webservices.WsReadAttribute
title: WsReadAttribute function
author: windows-sdk-content
description: Read an attribute producing a value of the specified WS_TYPE.
old-location: wsw\wsreadattribute.htm
tech.root: wsw
ms.assetid: 2055182a-8aff-4db0-88f1-d344ca89e383
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WsReadAttribute, WsReadAttribute function [Web Services for Windows], webservices/WsReadAttribute, wsw.wsreadattribute
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
 - WsReadAttribute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsReadAttribute function


## -description


Read an attribute producing a value of the specified <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_TYPE</a>.
            


## -parameters




### -param reader [in]

The reader that is positioned on the element containing the attribute.
                


### -param attributeDescription [in]

A pointer to a description of how to deserialize the attribute.
                


### -param readOption [in]

Whether the attribute is required, and how to allocate the value.
                    See <a href="https://msdn.microsoft.com/634b057f-3121-43cc-919f-8636e67ce0d7">WS_READ_OPTION</a> for more information.
                


### -param heap [in, optional]

The heap to store the deserialized values in.
                


### -param value

The interpretation of this parameter depends on the <a href="https://msdn.microsoft.com/634b057f-3121-43cc-919f-8636e67ce0d7">WS_READ_OPTION</a>.
                


### -param valueSize [in]

The interpretation of this parameter depends on the <a href="https://msdn.microsoft.com/634b057f-3121-43cc-919f-8636e67ce0d7">WS_READ_OPTION</a>.
                


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
<dt><b>WS_E_QUOTA_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
The size quota of the heap was exceeded.
                

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
</table>
 




## -remarks



This API will search for the attribute given the name and namespace, and then
                and deserialize the content as a typed value.
            

If the API fails, the state of input reader becomes undefined. The only APIs that may be used on the reader
        if this occurs are <a href="https://msdn.microsoft.com/d7ac5233-266e-4ca1-aa58-e50b385b48bb">WsSetInput</a> and <a href="https://msdn.microsoft.com/0b3ac6ab-8c16-4189-950d-84bdcdabcde0">WsSetInputToBuffer</a> to return the reader to a usable state,
        or <a href="https://msdn.microsoft.com/31163bea-266f-43a3-bdf5-61386ebc197c">WsFreeReader</a> to free the reader.
            



