---
UID: NF:webservices.WsSetErrorProperty
title: WsSetErrorProperty function
author: windows-sdk-content
description: Sets an WS_ERROR object property.
old-location: wsw\wsseterrorproperty.htm
old-project: wsw
ms.assetid: 5193eaf4-29f7-4e97-a3b0-97441b26399c
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: WsSetErrorProperty, WsSetErrorProperty function [Web Services for Windows], webservices/WsSetErrorProperty, wsw.wsseterrorproperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WS_SECURITY_ALGORITHM_PROPERTY_ID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsSetErrorProperty
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsSetErrorProperty function


## -description



                Sets an <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object property. 


## -parameters




### -param error [in]

A pointer to the <b>Error</b> object in which to set the property.  The pointer must reference a valid <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object.
                


### -param id [in]

Identifier of the property to set.
                


### -param value

A pointer to the property value to set.
                    The pointer must have an alignment compatible with the type
                    of the property.
                


### -param valueSize [in]

The size in bytes of the property value.
                


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
The property id was not supported for this object.

The specified size was not appropriate for the property.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was not enough space to set the property value.

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
 



