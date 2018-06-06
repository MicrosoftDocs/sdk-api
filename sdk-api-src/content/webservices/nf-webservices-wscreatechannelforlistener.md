---
UID: NF:webservices.WsCreateChannelForListener
title: WsCreateChannelForListener function
author: windows-sdk-content
description: Creates a channel associated with a specified listener.
old-location: wsw\wscreatechannelforlistener.htm
old-project: wsw
ms.assetid: d9a80506-d891-4cfd-b120-0d3fce946cf5
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WsCreateChannelForListener, WsCreateChannelForListener function [Web Services for Windows], webservices/WsCreateChannelForListener, wsw.wscreatechannelforlistener
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: WS_SECURITY_ALGORITHM_PROPERTY_ID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsCreateChannelForListener
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsCreateChannelForListener function


## -description


Creates a <a href="https://msdn.microsoft.com/5a04580d-c89f-4505-a4b7-0724ffb788fd">channel</a> associated with a specified <a href="https://msdn.microsoft.com/fffda587-23f5-4c7a-93c5-f03d9d3fafb2">listener</a>.


## -parameters




### -param listener [in]

Pointer to a <a href="https://msdn.microsoft.com/2e771c56-4a07-4c8e-92c1-ffcbf74cd1aa">WS_LISTENER</a> structure representing the listener for which to create a channel.  The listener 
                    can be in any state. (For listener states, see the <a href="https://msdn.microsoft.com/275d0d36-f9a1-49a7-af74-e8967dff574a">WS_LISTENER_STATE</a>  enumeration.)


### -param properties

An array of  <a href="https://msdn.microsoft.com/0298e8ae-67ad-4881-885f-2ed713316e76">WS_CHANNEL_PROPERTY</a> structures containing optional values for channel initialization.  This can be a <b>NULL</b>, in which case, the <i>propertyCount</i> parameter must be 0 (zero).
                

For information on creating a custom channel, see the Remarks section.


### -param propertyCount [in]

The number of  properties in the <i>properties</i> array.
                


### -param channel


                    On success, a pointer that receives the address of the created channel.   
                    When the channel  is no longer needed, you must free  it by calling <a href="https://msdn.microsoft.com/74e36d19-c6db-4bba-90e3-88a48b6a1fb5">WsFreeChannel</a>.
                


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
 




## -remarks




                To accept an incoming message exchange, call the <a href="https://msdn.microsoft.com/e18e0005-89bd-435e-9a12-6602c3c638b7">WsAcceptChannel</a> function.
            


                The security characteristics of the channel are the same as those 
                specified for the listener.
            

When you create a custom channel (using the WS_CUSTOM_CHANNEL_BINDING value of the <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_CHANNEL_BINDING</a> enumeration), you can specify only the following channel properties: 

<ul>
<li>WS_CHANNEL_PROPERTY_CUSTOM_CHANNEL_CALLBACKS </li>
<li>WS_CHANNEL_PROPERTY_CUSTOM_CHANNEL_PARAMETERS</li>
</ul>If initial properties are required to create the custom channel, specify them by using the WS_CHANNEL_PROPERTY_CUSTOM_CHANNEL_PARAMETERS property. 





