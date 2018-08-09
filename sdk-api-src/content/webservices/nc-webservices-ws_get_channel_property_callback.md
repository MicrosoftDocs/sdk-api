---
UID: NC:webservices.WS_GET_CHANNEL_PROPERTY_CALLBACK
title: WS_GET_CHANNEL_PROPERTY_CALLBACK
author: windows-sdk-content
description: Handles the WsGetChannelProperty call for a WS_CUSTOM_CHANNEL_BINDING.
old-location: wsw\ws_get_channel_property_callback.htm
old-project: wsw
ms.assetid: 8fd503a9-6f8d-46c3-9338-c900b9b1d747
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WS_GET_CHANNEL_PROPERTY_CALLBACK, WS_GET_CHANNEL_PROPERTY_CALLBACK callback, WS_GET_CHANNEL_PROPERTY_CALLBACK callback function [Web Services for Windows], webservices/WS_GET_CHANNEL_PROPERTY_CALLBACK, wsw.ws_get_channel_property_callback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: WDSTRANSPORT_TFTP_CAPABILITY, *PWDSTRANSPORT_TFTP_CAPABILITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WebServices.h
api_name:
 - WS_GET_CHANNEL_PROPERTY_CALLBACK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_GET_CHANNEL_PROPERTY_CALLBACK callback function


## -description


Handles the <a href="https://msdn.microsoft.com/6f3440d2-90cc-4312-bb08-51f08b864cc7">WsGetChannelProperty</a> call
                for a <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_CUSTOM_CHANNEL_BINDING</a>.
            


## -parameters




### -param *channelInstance [in]

The pointer to the state specific to this channel instance,
                    as created by the <a href="https://msdn.microsoft.com/440114f9-2258-4c33-93cd-7185ccf36f76">WS_CREATE_CHANNEL_CALLBACK</a>.
                


### -param id [in]

The id of the property to retrieve.
                


### -param *value

The location to store the retrieved property.
                    The pointer must have an alignment compatible with the type
                    of the property.
                


### -param valueSize [in]

The number of bytes allocated by the caller to
                    store the retrieved property.
                


### -param *error [in, optional]

Specifies where additional error information should be stored if the function fails.
                


## -returns



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
 




## -remarks



See <a href="https://msdn.microsoft.com/6f3440d2-90cc-4312-bb08-51f08b864cc7">WsGetChannelProperty</a> for information about the contract
                of this API.
            

Every custom channel implementation must support returning
                a value for at least the following properties:
            

<ul>
<li>
<a href="https://msdn.microsoft.com/3207c7f0-7f12-4f6b-8ddd-bac9c06ccfbf">WS_CHANNEL_PROPERTY_ADDRESSING_VERSION</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3207c7f0-7f12-4f6b-8ddd-bac9c06ccfbf">WS_CHANNEL_PROPERTY_ENVELOPE_VERSION</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3207c7f0-7f12-4f6b-8ddd-bac9c06ccfbf">WS_CHANNEL_PROPERTY_TRANSFER_MODE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3207c7f0-7f12-4f6b-8ddd-bac9c06ccfbf">WS_CHANNEL_PROPERTY_PROTECTION_LEVEL</a>
</li>
</ul>
Service Model layer provides its own logic of call timeouts as such it requires 
                disabling timeouts in the underlying channel. In order for a custom channel to be 
                used from Service Model layer, it should support disabling all of its timeouts and 
                implement this callback for <a href="https://msdn.microsoft.com/3207c7f0-7f12-4f6b-8ddd-bac9c06ccfbf">WS_CHANNEL_PROPERTY_ENABLE_TIMEOUTS</a>. A custom 
                channel cannot be used through Service Model unless query for 
                <b>WS_CHANNEL_PROPERTY_ENABLE_TIMEOUTS</b> returns <b>FALSE</b>.
            

It is up to the custom channel implementation to determine any
                additional properties it wishes to support.
            

If a property is not supported, the <b>E_INVALIDARG</b> should be returned.
             (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.)



