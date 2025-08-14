---
UID: NF:winevt.EvtOpenChannelEnum
title: EvtOpenChannelEnum function (winevt.h)
description: Gets a handle that you use to enumerate the list of channels that are registered on the computer.
helpviewer_keywords: ["EvtOpenChannelEnum","EvtOpenChannelEnum function [EventLog]","wes.evtopenchannelenum","winevt/EvtOpenChannelEnum"]
old-location: wes\evtopenchannelenum.htm
tech.root: wes
ms.assetid: eb077b0c-1ae6-40ae-becc-98d840302e6f
ms.date: 12/05/2018
ms.keywords: EvtOpenChannelEnum, EvtOpenChannelEnum function [EventLog], wes.evtopenchannelenum, winevt/EvtOpenChannelEnum
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
 - EvtOpenChannelEnum
 - winevt/EvtOpenChannelEnum
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
api_name:
 - EvtOpenChannelEnum
---

# EvtOpenChannelEnum function


## -description

Gets a handle that you use to enumerate the list of channels that are registered on the computer.

## -parameters

### -param Session [in]

A remote session handle that the <a href="/windows/desktop/api/winevt/nf-winevt-evtopensession">EvtOpenSession</a> function returns. Set to <b>NULL</b> to enumerate the channels on the local computer.

### -param Flags [in]

Reserved. Must be zero.

## -returns

If successful, the function returns a handle to the list of channel names that are registered on the computer; otherwise, <b>NULL</b>. If <b>NULL</b>, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function to get the error code.

## -remarks

The enumeration includes all the channels that the providers that are registered on the computer defined. To enumerate the channel names, call the <a href="/windows/desktop/api/winevt/nf-winevt-evtnextchannelpath">EvtNextChannelPath</a> function in a loop. The names are sorted alphabetically.

You must call the <a href="/windows/desktop/api/winevt/nf-winevt-evtclose">EvtClose</a> function to close the enumerator handle when done.


#### Examples

For an example that shows how to use this function, see <a href="/windows/desktop/WES/getting-and-setting-a-channel-s-configuration-properties">Getting and Setting a Channel's Configuration Properties</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winevt/nf-winevt-evtnextchannelpath">EvtNextChannelPath</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtopenchannelconfig">EvtOpenChannelConfig</a>