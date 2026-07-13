---
UID: NF:winevt.EvtSetChannelConfigProperty
title: EvtSetChannelConfigProperty function (winevt.h)
description: Sets the specified configuration property of a channel.
helpviewer_keywords: ["EvtSetChannelConfigProperty","EvtSetChannelConfigProperty function [EventLog]","wes.evtsetchannelconfigproperty","winevt/EvtSetChannelConfigProperty"]
old-location: wes\evtsetchannelconfigproperty.htm
tech.root: wes
ms.assetid: f5f11bd9-5eb0-4afe-8c8b-57fa3850ad56
ms.date: 12/05/2018
ms.keywords: EvtSetChannelConfigProperty, EvtSetChannelConfigProperty function [EventLog], wes.evtsetchannelconfigproperty, winevt/EvtSetChannelConfigProperty
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EvtSetChannelConfigProperty
 - winevt/EvtSetChannelConfigProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-wevtapi-eventlog-l1-1-3.dll
 - Wevtapi.dll
 - Ext-MS-Win-WEvtAPI-EventLog-L1-1-2.dll
api_name:
 - EvtSetChannelConfigProperty
---

# EvtSetChannelConfigProperty function


## -description

Sets the specified configuration property of a channel.

## -parameters

### -param ChannelConfig [in]

A handle to the channel's configuration properties that the  <a href="/windows/desktop/api/winevt/nf-winevt-evtopenchannelconfig">EvtOpenChannelConfig</a> function returns.

### -param PropertyId [in]

The identifier of the channel property to set. For a list of property identifiers, see the <a href="/windows/desktop/api/winevt/ne-winevt-evt_channel_config_property_id">EVT_CHANNEL_CONFIG_PROPERTY_ID</a> enumeration.

### -param Flags [in]

Reserved. Must be zero.

### -param PropertyValue [in]

The property value to set.

A caller-allocated buffer that contains the new configuration property value. The buffer contains an <a href="/windows/desktop/api/winevt/ns-winevt-evt_variant">EVT_VARIANT</a> object. Be sure to set the configuration value and variant type.

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
The function failed. To get the error code, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

</td>
</tr>
</table>

## -remarks

This function changes an in-memory copy of the configuration properties. To apply the changes that you have made to one or more of the configuration properties, call the  <a href="/windows/desktop/api/winevt/nf-winevt-evtsavechannelconfig">EvtSaveChannelConfig</a> function.


#### Examples

For an example that shows how to use this function, see <a href="/windows/desktop/WES/getting-and-setting-a-channel-s-configuration-properties">Getting and Setting a Channel's Configuration Properties</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winevt/nf-winevt-evtgetchannelconfigproperty">EvtGetChannelConfigProperty</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtopenchannelconfig">EvtOpenChannelConfig</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtsavechannelconfig">EvtSaveChannelConfig</a>