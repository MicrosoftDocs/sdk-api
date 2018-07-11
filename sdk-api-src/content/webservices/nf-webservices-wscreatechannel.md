---
UID: NF:webservices.WsCreateChannel
title: WsCreateChannel function
author: windows-sdk-content
description: Creates a channel for message exchange with an endpoint.
old-location: wsw\wscreatechannel.htm
old-project: wsw
ms.assetid: 4bef6f97-06f1-442a-8b84-869776f0541d
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: WsCreateChannel, WsCreateChannel function [Web Services for Windows], webservices/WsCreateChannel, wsw.wscreatechannel
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
 - WsCreateChannel
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsCreateChannel function


## -description



Creates a <a href="https://msdn.microsoft.com/5a04580d-c89f-4505-a4b7-0724ffb788fd">channel</a> for message exchange with an endpoint.  
            




## -parameters




### -param channelType [in]

The type of the channel. For channel types, see the <a href="https://msdn.microsoft.com/7e1092f9-10e8-485c-a286-770e1c74d8ca">WS_CHANNEL_TYPE</a> enumeration. This represents the message exchange pattern for the channel being created.
        


### -param channelBinding [in]

The channel <a href="https://msdn.microsoft.com/library/windows/hardware/mt270133">binding</a>, indicating the protocol stack to use for the new channel.
                For available channel bindings, see the <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_CHANNEL_BINDING</a> enumeration.


### -param properties [in]

An array of  <a href="https://msdn.microsoft.com/0298e8ae-67ad-4881-885f-2ed713316e76">WS_CHANNEL_PROPERTY</a>  structures  containing optional values for channel initialization.  The value of this parameter may be <b>NULL</b>, in which case, the <i>propertyCount</i> parameter must be 0 (zero).
                

For information on which channel properties can be specified when you create a channel, see the <a href="https://msdn.microsoft.com/3207c7f0-7f12-4f6b-8ddd-bac9c06ccfbf">WS_CHANNEL_PROPERTY_ID</a> enumeration.

For information on creating a custom channel, see the Remarks section.


### -param propertyCount [in]

The number of properties in the <i>properties</i> array.
                


### -param securityDescription [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/b9490f00-877c-4d9f-b361-eaca343cdee0">WS_SECURITY_DESCRIPTION</a>  structure specifying the security for the channel.

If you are creating a custom channel (using the WS_CUSTOM_CHANNEL_BINDING value of the <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_CHANNEL_BINDING</a> enumeration), the security description must be <b>NULL</b>. See the Remarks section.


### -param channel


                    Pointer that receives the address of the created channel.   
                    When the channel  is no longer needed, you must free  it by calling <a href="https://msdn.microsoft.com/74e36d19-c6db-4bba-90e3-88a48b6a1fb5">WsFreeChannel</a>.
                


### -param error [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> structure that receives additional error information if the function fails.
                


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
 




## -remarks




                Use the <a href="https://msdn.microsoft.com/a7226194-0974-4f3c-b92d-78a93e86eea5">WsOpenChannel</a> function to initiate  communication on the channel and to specify the endpoint.
            

When you create a custom channel (using the WS_CUSTOM_CHANNEL_BINDING value of the <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_CHANNEL_BINDING</a> enumeration), you can specify only the following channel properties: 

<ul>
<li>WS_CHANNEL_PROPERTY_CUSTOM_CHANNEL_CALLBACKS </li>
<li>WS_CHANNEL_PROPERTY_CUSTOM_CHANNEL_PARAMETERS</li>
</ul>(See the <a href="https://msdn.microsoft.com/3207c7f0-7f12-4f6b-8ddd-bac9c06ccfbf">WS_CHANNEL_PROPERTY_ID</a> enumeration) If initial properties are required to create the custom channel, specify them by using the WS_CHANNEL_PROPERTY_CUSTOM_CHANNEL_PARAMETERS property. 



To pass security information to a custom channel implementation, use the WS_CHANNEL_PROPERTY_CUSTOM_CHANNEL_PARAMETERS value of the  <a href="https://msdn.microsoft.com/3207c7f0-7f12-4f6b-8ddd-bac9c06ccfbf">WS_CHANNEL_PROPERTY_ID</a> enumeration.



