---
UID: NF:winevt.EvtSaveChannelConfig
title: EvtSaveChannelConfig function
author: windows-sdk-content
description: Saves the changes made to a channel's configuration.
old-location: wes\evtsavechannelconfig.htm
old-project: WES
ms.assetid: 3f3eff67-24b6-448e-bb61-0bc851d9bdfa
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: EvtSaveChannelConfig, EvtSaveChannelConfig function [EventLog], wes.evtsavechannelconfig, winevt/EvtSaveChannelConfig
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: EVT_VARIANT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wevtapi.dll
 - Ext-MS-Win-WEvtAPI-EventLog-L1-1-2.dll
api_name:
 - EvtSaveChannelConfig
product: Windows
targetos: Windows
req.lib: Wevtapi.lib
req.dll: Wevtapi.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# EvtSaveChannelConfig function


## -description


Saves the changes made to a channel's configuration.


## -parameters




### -param ChannelConfig [in]

A handle to the channel's configuration properties that the  <a href="https://msdn.microsoft.com/d197f04e-01e8-4ef6-a9ca-61e5178d825b">EvtOpenChannelConfig</a> function returns.


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
The function failed. To get the error code, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

</td>
</tr>
</table>
 




## -remarks



To change a channel's configuration property, call the <a href="https://msdn.microsoft.com/f5f11bd9-5eb0-4afe-8c8b-57fa3850ad56">EvtSetChannelConfigProperty</a> function.

You must call this function with elevated permissions; otherwise, this function returns ERROR_ACCESS_DENIED.


#### Examples

For an example that shows how to use this function, see <a href="https://msdn.microsoft.com/4ee44dae-b390-4d98-bcef-836b53b04860">Getting and Setting a Channel's Configuration Properties</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/f5f11bd9-5eb0-4afe-8c8b-57fa3850ad56">EvtSetChannelConfigProperty</a>
 

 

