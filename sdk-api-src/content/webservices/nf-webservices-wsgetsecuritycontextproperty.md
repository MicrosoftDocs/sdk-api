---
UID: NF:webservices.WsGetSecurityContextProperty
title: WsGetSecurityContextProperty function
author: windows-sdk-content
description: Gets a property of the specified security context.
old-location: wsw\wsgetsecuritycontextproperty.htm
tech.root: wsw
ms.assetid: 7ef32fbe-0b50-4ede-96af-075137df340d
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: WsGetSecurityContextProperty, WsGetSecurityContextProperty function [Web Services for Windows], webservices/WsGetSecurityContextProperty, wsw.wsgetsecuritycontextproperty
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
 - WsGetSecurityContextProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsGetSecurityContextProperty function


## -description


Gets a property of the specified security context.
      


## -parameters




### -param securityContext [in]

The security context that is queried for its property.
        


### -param id [in]

The id of the property (one of <a href="https://msdn.microsoft.com/fd2b92d4-9834-4d4b-85c3-8ea8d2c8bd8c">WS_SECURITY_CONTEXT_PROPERTY_ID</a>).
        


### -param value

The address to place the retrieved value. The pointer must have an alignment compatible with the type of the property.
        


### -param valueSize [in]

The size of the buffer that the caller has allocated for the retrieved value.
        


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
The property id was not supported for this object or the specified buffer was not large enough for the value.

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
 



