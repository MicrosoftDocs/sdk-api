---
UID: NF:winevt.EvtNextChannelPath
title: EvtNextChannelPath function
author: windows-sdk-content
description: Gets a channel name from the enumerator.
old-location: wes\evtnextchannelpath.htm
tech.root: wes
ms.assetid: 51fd2449-8a89-4a18-99c3-b974c2c998ca
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EvtNextChannelPath, EvtNextChannelPath function [EventLog], wes.evtnextchannelpath, winevt/EvtNextChannelPath
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
api_name:
 - EvtNextChannelPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EvtNextChannelPath function


## -description


Gets a channel name from the enumerator.


## -parameters




### -param ChannelEnum [in]

A handle to the enumerator that the <a href="https://msdn.microsoft.com/eb077b0c-1ae6-40ae-becc-98d840302e6f">EvtOpenChannelEnum</a> function returns.


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
The function failed. To get the error code, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

</td>
</tr>
</table>
 




## -remarks



Call this function in a loop until the function returns <b>FALSE</b> and the error code is ERROR_NO_MORE_ITEMS.


#### Examples

For an example that shows how to use this function, see <a href="https://msdn.microsoft.com/4ee44dae-b390-4d98-bcef-836b53b04860">Getting and Setting a Channel's Configuration Properties</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/eb077b0c-1ae6-40ae-becc-98d840302e6f">EvtOpenChannelEnum</a>
 

 

