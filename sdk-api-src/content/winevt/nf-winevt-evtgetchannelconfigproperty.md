---
UID: NF:winevt.EvtGetChannelConfigProperty
title: EvtGetChannelConfigProperty function
author: windows-sdk-content
description: Gets the specified channel configuration property.
old-location: wes\evtgetchannelconfigproperty.htm
tech.root: wes
ms.assetid: 0f84f51c-716e-4a70-b31c-2b4f40b3fd83
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EvtGetChannelConfigProperty, EvtGetChannelConfigProperty function [EventLog], wes.evtgetchannelconfigproperty, winevt/EvtGetChannelConfigProperty
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
req.lib: Wevtapi.lib
req.dll: Wevtapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wevtapi.dll
 - Ext-MS-Win-WEvtAPI-EventLog-L1-1-0.dll
 - Ext-MS-Win-WEvtAPI-EventLog-L1-1-1.dll
 - Ext-MS-Win-WEvtAPI-EventLog-L1-1-2.dll
api_name:
 - EvtGetChannelConfigProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EvtGetChannelConfigProperty function


## -description


Gets the specified channel configuration property.


## -parameters




### -param ChannelConfig [in]

A handle to the channel's configuration properties that the  <a href="https://msdn.microsoft.com/d197f04e-01e8-4ef6-a9ca-61e5178d825b">EvtOpenChannelConfig</a> function returns.


### -param PropertyId [in]

The identifier of the channel property to retrieve. For a list of property identifiers, see the <a href="https://msdn.microsoft.com/ea17cbf8-ab60-4bf9-b0a2-998814a50bd0">EVT_CHANNEL_CONFIG_PROPERTY_ID</a> enumeration.


### -param Flags [in]

Reserved. Must be zero.


### -param PropertyValueBufferSize [in]

The size of the <i>PropertyValueBuffer</i> buffer, in bytes.


### -param PropertyValueBuffer [in]

A caller-allocated buffer that will receive the configuration property. The buffer contains an <a href="https://msdn.microsoft.com/4b0f338b-0b66-4ba5-9e29-b15afe15a2d3">EVT_VARIANT</a> object. You can set this parameter to <b>NULL</b> to determine the required buffer size.


### -param PropertyValueBufferUsed [out]

The size, in bytes, of the caller-allocated buffer that the function used or the required buffer size if the function fails with ERROR_INSUFFICIENT_BUFFER.


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
 




## -see-also




<a href="https://msdn.microsoft.com/d197f04e-01e8-4ef6-a9ca-61e5178d825b">EvtOpenChannelConfig</a>
 

 

