---
UID: NF:webservices.WsSetChannelProperty
title: WsSetChannelProperty function
author: windows-sdk-content
description: Sets a property of the channel.
old-location: wsw\wssetchannelproperty.htm
tech.root: wsw
ms.assetid: 0bf3ec1b-c711-4c26-9c54-5d0184c89871
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WsSetChannelProperty, WsSetChannelProperty function [Web Services for Windows], webservices/WsSetChannelProperty, wsw.wssetchannelproperty
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
 - WsSetChannelProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsSetChannelProperty function


## -description


Sets a property of the channel.
            


## -parameters




### -param channel [in]

A pointer to the <b>Channel</b> on which to set the property and may not be <b>NULL</b>.


### -param id [in]

Identifier of the property to set.
                


### -param value

A void pointer to the property value to set.
                    The pointer must have an alignment compatible with the type
                    of the property.
                


### -param valueSize [in]

The size in bytes of of the property value.
                


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
 



