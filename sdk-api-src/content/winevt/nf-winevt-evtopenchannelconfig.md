---
UID: NF:winevt.EvtOpenChannelConfig
title: EvtOpenChannelConfig function (winevt.h)
description: Gets a handle that you use to read or modify a channel's configuration property.
helpviewer_keywords: ["EvtOpenChannelConfig","EvtOpenChannelConfig function [EventLog]","wes.evtopenchannelconfig","winevt/EvtOpenChannelConfig"]
old-location: wes\evtopenchannelconfig.htm
tech.root: wes
ms.assetid: d197f04e-01e8-4ef6-a9ca-61e5178d825b
ms.date: 12/05/2018
ms.keywords: EvtOpenChannelConfig, EvtOpenChannelConfig function [EventLog], wes.evtopenchannelconfig, winevt/EvtOpenChannelConfig
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
 - EvtOpenChannelConfig
 - winevt/EvtOpenChannelConfig
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
 - EvtOpenChannelConfig
---

# EvtOpenChannelConfig function


## -description

Gets a handle that you use to read or modify a channel's configuration property.

## -parameters

### -param Session [in]

A remote session handle that the <a href="/windows/desktop/api/winevt/nf-winevt-evtopensession">EvtOpenSession</a> function returns. Set to <b>NULL</b> to access a channel on the local computer.

### -param ChannelPath [in]

The name of the channel to access.

### -param Flags [in]

Reserved. Must be zero.

## -returns

If successful, the function returns a handle to the channel's configuration; otherwise, <b>NULL</b>. If <b>NULL</b>, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function to get the error code.

## -remarks

To get a configuration property, call the <a href="/windows/desktop/api/winevt/nf-winevt-evtgetchannelconfigproperty">EvtGetChannelConfigProperty</a> function.

To modify a configuration property, call the <a href="/windows/desktop/api/winevt/nf-winevt-evtsetchannelconfigproperty">EvtSetChannelConfigProperty</a> function. To save the configuration changes, call the <a href="/windows/desktop/api/winevt/nf-winevt-evtsavechannelconfig">EvtSaveChannelConfig</a> function.

To enumerate the registered channels, call the <a href="/windows/desktop/api/winevt/nf-winevt-evtopenchannelenum">EvtOpenChannelEnum</a> function.

You must call the <a href="/windows/desktop/api/winevt/nf-winevt-evtclose">EvtClose</a> function to close the handle when done.


#### Examples

For an example that shows how to use this function, see <a href="/windows/desktop/WES/getting-and-setting-a-channel-s-configuration-properties">Getting and Setting a Channel's Configuration Properties</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winevt/nf-winevt-evtgetchannelconfigproperty">EvtGetChannelConfigProperty</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtopenchannelenum">EvtOpenChannelEnum</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtsavechannelconfig">EvtSaveChannelConfig</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtsetchannelconfigproperty">EvtSetChannelConfigProperty</a>