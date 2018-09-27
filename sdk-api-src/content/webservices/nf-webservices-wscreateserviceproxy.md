---
UID: NF:webservices.WsCreateServiceProxy
title: WsCreateServiceProxy function
author: windows-sdk-content
description: Creates a service proxy with the specified properties.
old-location: wsw\wscreateserviceproxy.htm
tech.root: wsw
ms.assetid: 9215684b-979e-48ad-b4ee-2ae1db1e3034
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: WsCreateServiceProxy, WsCreateServiceProxy function [Web Services for Windows], webservices/WsCreateServiceProxy, wsw.wscreateserviceproxy
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
 - WsCreateServiceProxy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsCreateServiceProxy function


## -description



Creates a  <a href="https://msdn.microsoft.com/e1a5bf5e-dbc1-43e3-981b-7db4caa08bdc">service proxy</a> with the specified properties.
            




## -parameters




### -param channelType [in]

A <a href="https://msdn.microsoft.com/7e1092f9-10e8-485c-a286-770e1c74d8ca">WS_CHANNEL_TYPE</a> enumeration value representing the channel type for the service proxy.
                


### -param channelBinding [in]

A <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_CHANNEL_BINDING</a> enumeration value representing the channel binding.
                


### -param securityDescription [in, optional]

A <a href="https://msdn.microsoft.com/b9490f00-877c-4d9f-b361-eaca343cdee0">WS_SECURITY_DESCRIPTION</a> structure representing the security description.
                


### -param properties

An array of <a href="https://msdn.microsoft.com/eb8ce473-bf9e-4eae-8c40-8e2972a26d41">WS_PROXY_PROPERTY</a> structures containing optional properties for the service proxy.

The value of this parameter may be <b>NULL</b>, in which case, the <i>propertyCount</i> parameter must be 0 (zero).
                


### -param propertyCount [in]

The number of properties in the <i>properties</i> array.
                


### -param channelProperties

An array of  <a href="https://msdn.microsoft.com/0298e8ae-67ad-4881-885f-2ed713316e76">WS_CHANNEL_PROPERTY</a>  structures containing optional channel properties.  The value of this parameter may be <b>NULL</b>, in which case, the <i>channelPropertyCount</i> parameter must be 0 (zero).
                

<div class="alert"><b>Note</b>  Be very careful about modifying the default values for these properties.</div>
<div> </div>

### -param channelPropertyCount [in]

The number of properties in the <i>channelProperties</i> array.
                
            


### -param serviceProxy

On   success, a pointer that receives the address of the  <a href="https://msdn.microsoft.com/623766ae-fe82-40f9-93c8-e78fe48bc6d1">WS_SERVICE_PROXY</a> structure representing the new service proxy.
                
                When you no longer need this structure, you must free it by calling <a href="https://msdn.microsoft.com/fb200cf8-c1d4-4a97-afef-f7c4ed5efb10">WsFreeServiceProxy</a>.
            


### -param error [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> structure  that receives additional error information if the function fails.
                
                


## -returns



If the function succeeds, it returns NO_ERROR; otherwise, it returns an HRESULT error code.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

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
 



