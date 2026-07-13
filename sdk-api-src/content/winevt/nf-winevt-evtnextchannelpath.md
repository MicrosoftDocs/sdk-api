---
UID: NF:winevt.EvtNextChannelPath
title: EvtNextChannelPath function (winevt.h)
description: Gets a channel name from the enumerator.
helpviewer_keywords: ["EvtNextChannelPath","EvtNextChannelPath function [EventLog]","wes.evtnextchannelpath","winevt/EvtNextChannelPath"]
old-location: wes\evtnextchannelpath.htm
tech.root: wes
ms.assetid: 51fd2449-8a89-4a18-99c3-b974c2c998ca
ms.date: 12/05/2018
ms.keywords: EvtNextChannelPath, EvtNextChannelPath function [EventLog], wes.evtnextchannelpath, winevt/EvtNextChannelPath
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
 - EvtNextChannelPath
 - winevt/EvtNextChannelPath
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
 - EvtNextChannelPath
---

# EvtNextChannelPath function


## -description

Gets a channel name from the enumerator.

## -parameters

### -param ChannelEnum [in]

A handle to the enumerator that the <a href="/windows/desktop/api/winevt/nf-winevt-evtopenchannelenum">EvtOpenChannelEnum</a> function returns.

### -param ChannelPathBufferSize [in]

The size of the <i>ChannelPathBuffer</i> buffer, in characters.

### -param ChannelPathBuffer [in]

A caller-allocated buffer that will receive the name of the channel. You can set this parameter to <b>NULL</b> to determine the required buffer size.

### -param ChannelPathBufferUsed [out]

The size, in characters, of the caller-allocated buffer that the function used or the required buffer size if the function fails with ERROR_INSUFFICIENT_BUFFER.

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

Call this function in a loop until the function returns <b>FALSE</b> and the error code is ERROR_NO_MORE_ITEMS.


#### Examples

For an example that shows how to use this function, see <a href="/windows/desktop/WES/getting-and-setting-a-channel-s-configuration-properties">Getting and Setting a Channel's Configuration Properties</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winevt/nf-winevt-evtopenchannelenum">EvtOpenChannelEnum</a>