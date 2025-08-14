---
UID: NF:winevt.EvtGetChannelConfigProperty
title: EvtGetChannelConfigProperty function (winevt.h)
description: Gets the specified channel configuration property.
helpviewer_keywords: ["EvtGetChannelConfigProperty","EvtGetChannelConfigProperty function [EventLog]","wes.evtgetchannelconfigproperty","winevt/EvtGetChannelConfigProperty"]
old-location: wes\evtgetchannelconfigproperty.htm
tech.root: wes
ms.assetid: 0f84f51c-716e-4a70-b31c-2b4f40b3fd83
ms.date: 12/05/2018
ms.keywords: EvtGetChannelConfigProperty, EvtGetChannelConfigProperty function [EventLog], wes.evtgetchannelconfigproperty, winevt/EvtGetChannelConfigProperty
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
 - EvtGetChannelConfigProperty
 - winevt/EvtGetChannelConfigProperty
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
 - Ext-MS-Win-WEvtAPI-EventLog-L1-1-0.dll
 - Ext-MS-Win-WEvtAPI-EventLog-L1-1-1.dll
 - Ext-MS-Win-WEvtAPI-EventLog-L1-1-2.dll
api_name:
 - EvtGetChannelConfigProperty
---

# EvtGetChannelConfigProperty function


## -description

Gets the specified channel configuration property.

## -parameters

### -param ChannelConfig [in]

A handle to the channel's configuration properties that the  <a href="/windows/desktop/api/winevt/nf-winevt-evtopenchannelconfig">EvtOpenChannelConfig</a> function returns.

### -param PropertyId [in]

The identifier of the channel property to retrieve. For a list of property identifiers, see the <a href="/windows/desktop/api/winevt/ne-winevt-evt_channel_config_property_id">EVT_CHANNEL_CONFIG_PROPERTY_ID</a> enumeration.

### -param Flags [in]

Reserved. Must be zero.

### -param PropertyValueBufferSize [in]

The size of the <i>PropertyValueBuffer</i> buffer, in bytes.

### -param PropertyValueBuffer [in]

A caller-allocated buffer that will receive the configuration property. The buffer contains an <a href="/windows/desktop/api/winevt/ns-winevt-evt_variant">EVT_VARIANT</a> object. You can set this parameter to <b>NULL</b> to determine the required buffer size.

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
The function failed. To get the error code, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winevt/nf-winevt-evtopenchannelconfig">EvtOpenChannelConfig</a>