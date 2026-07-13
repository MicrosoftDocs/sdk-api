---
UID: NF:winevt.EvtSaveChannelConfig
title: EvtSaveChannelConfig function (winevt.h)
description: Saves the changes made to a channel's configuration.
helpviewer_keywords: ["EvtSaveChannelConfig","EvtSaveChannelConfig function [EventLog]","wes.evtsavechannelconfig","winevt/EvtSaveChannelConfig"]
old-location: wes\evtsavechannelconfig.htm
tech.root: wes
ms.assetid: 3f3eff67-24b6-448e-bb61-0bc851d9bdfa
ms.date: 12/05/2018
ms.keywords: EvtSaveChannelConfig, EvtSaveChannelConfig function [EventLog], wes.evtsavechannelconfig, winevt/EvtSaveChannelConfig
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
 - EvtSaveChannelConfig
 - winevt/EvtSaveChannelConfig
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
 - EvtSaveChannelConfig
---

# EvtSaveChannelConfig function


## -description

Saves the changes made to a channel's configuration.

## -parameters

### -param ChannelConfig [in]

A handle to the channel's configuration properties that the  <a href="/windows/desktop/api/winevt/nf-winevt-evtopenchannelconfig">EvtOpenChannelConfig</a> function returns.

### -param Flags [in]

Reserved. Must be zero.

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

To change a channel's configuration property, call the <a href="/windows/desktop/api/winevt/nf-winevt-evtsetchannelconfigproperty">EvtSetChannelConfigProperty</a> function.

You must call this function with elevated permissions; otherwise, this function returns ERROR_ACCESS_DENIED.


#### Examples

For an example that shows how to use this function, see <a href="/windows/desktop/WES/getting-and-setting-a-channel-s-configuration-properties">Getting and Setting a Channel's Configuration Properties</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winevt/nf-winevt-evtsetchannelconfigproperty">EvtSetChannelConfigProperty</a>