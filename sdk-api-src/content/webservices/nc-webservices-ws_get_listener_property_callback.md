---
UID: NC:webservices.WS_GET_LISTENER_PROPERTY_CALLBACK
title: WS_GET_LISTENER_PROPERTY_CALLBACK
author: windows-sdk-content
description: Handles the WsGetListenerProperty call for a WS_CUSTOM_CHANNEL_BINDING.
old-location: wsw\ws_get_listener_property_callback.htm
old-project: wsw
ms.assetid: c2f79c5c-4a4f-4a45-ac70-432f818e7b46
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WS_GET_LISTENER_PROPERTY_CALLBACK, WS_GET_LISTENER_PROPERTY_CALLBACK callback, WS_GET_LISTENER_PROPERTY_CALLBACK callback function [Web Services for Windows], webservices/WS_GET_LISTENER_PROPERTY_CALLBACK, wsw.ws_get_listener_property_callback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: webservices.h
req.include-header: 
req.redist: 
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
 - WS_GET_LISTENER_PROPERTY_CALLBACK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_GET_LISTENER_PROPERTY_CALLBACK callback function


## -description


Handles the <a href="https://msdn.microsoft.com/cc4fb48a-8282-471a-aed0-1ca3134f9bd0">WsGetListenerProperty</a> call
                for a <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_CUSTOM_CHANNEL_BINDING</a>.
            


## -parameters




### -param *listenerInstance [in]

The pointer to the state specific to this listener instance,
                    as created by the <a href="https://msdn.microsoft.com/2d8e476d-dc68-44b4-b53b-be440a32efda">WS_CREATE_LISTENER_CALLBACK</a>.
                


### -param id [in]

The id of the property to retrieve.
                

A custom listener can decide which properties to support.
                


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
<dt><b> Other Errors </b></dt>
</dl>
</td>
<td width="60%">
This function may return other errors not listed above.

</td>
</tr>
</table>
 




## -remarks



See <a href="https://msdn.microsoft.com/cc4fb48a-8282-471a-aed0-1ca3134f9bd0">WsGetListenerProperty</a> for information about the contract
                of this API.
            



