---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# EvtSetChannelConfigProperty function


## -description


Sets the specified configuration property of a channel.


## -parameters




### -param ChannelConfig [in]

A handle to the channel's configuration properties that the  <a href="https://msdn.microsoft.com/d197f04e-01e8-4ef6-a9ca-61e5178d825b">EvtOpenChannelConfig</a> function returns.


### -param PropertyId [in]

The identifier of the channel property to set. For a list of property identifiers, see the <a href="https://msdn.microsoft.com/ea17cbf8-ab60-4bf9-b0a2-998814a50bd0">EVT_CHANNEL_CONFIG_PROPERTY_ID</a> enumeration.


### -param Flags [in]

Reserved. Must be zero.


### -param PropertyValue [in]

The property value to set.


A caller-allocated buffer that contains the new configuration property value. The buffer contains an <a href="https://msdn.microsoft.com/4b0f338b-0b66-4ba5-9e29-b15afe15a2d3">EVT_VARIANT</a> object. Be sure to set the configuration value and variant type.


## -returns



<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The function failed. To get the error code, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

</td>
</tr>
</table>
 




## -remarks



This function changes an in-memory copy of the configuration properties. To apply the changes that you have made to one or more of the configuration properties, call the  <a href="https://msdn.microsoft.com/3f3eff67-24b6-448e-bb61-0bc851d9bdfa">EvtSaveChannelConfig</a> function.


#### Examples

For an example that shows how to use this function, see <a href="https://msdn.microsoft.com/4ee44dae-b390-4d98-bcef-836b53b04860">Getting and Setting a Channel's Configuration Properties</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0f84f51c-716e-4a70-b31c-2b4f40b3fd83">EvtGetChannelConfigProperty</a>



<a href="https://msdn.microsoft.com/d197f04e-01e8-4ef6-a9ca-61e5178d825b">EvtOpenChannelConfig</a>



<a href="https://msdn.microsoft.com/3f3eff67-24b6-448e-bb61-0bc851d9bdfa">EvtSaveChannelConfig</a>
 

 

