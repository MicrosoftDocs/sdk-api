---
UID: NF:winevt.EvtSetChannelConfigProperty
title: EvtSetChannelConfigProperty function
author: windows-driver-content
description: Sets the specified configuration property of a channel.
old-location: wes\evtsetchannelconfigproperty.htm
old-project: WES
ms.assetid: f5f11bd9-5eb0-4afe-8c8b-57fa3850ad56
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: EvtSetChannelConfigProperty, EvtSetChannelConfigProperty function [EventLog], wes.evtsetchannelconfigproperty, winevt/EvtSetChannelConfigProperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winevt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: EVT_VARIANT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wevtapi.dll
-	Ext-MS-Win-WEvtAPI-EventLog-L1-1-2.dll
api_name:
-	EvtSetChannelConfigProperty
product: Windows
targetos: Windows
req.lib: Wevtapi.lib
req.dll: Wevtapi.dll
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

