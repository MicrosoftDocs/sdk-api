---
UID: NF:winevt.EvtOpenChannelConfig
title: EvtOpenChannelConfig function
author: windows-sdk-content
description: Gets a handle that you use to read or modify a channel's configuration property.
old-location: wes\evtopenchannelconfig.htm
old-project: WES
ms.assetid: d197f04e-01e8-4ef6-a9ca-61e5178d825b
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: EvtOpenChannelConfig, EvtOpenChannelConfig function [EventLog], wes.evtopenchannelconfig, winevt/EvtOpenChannelConfig
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
 - Ext-MS-Win-WEvtAPI-EventLog-L1-1-0.dll
 - Ext-MS-Win-WEvtAPI-EventLog-L1-1-1.dll
 - Ext-MS-Win-WEvtAPI-EventLog-L1-1-2.dll
api_name:
 - EvtOpenChannelConfig
product: Windows
targetos: Windows
req.lib: Wevtapi.lib
req.dll: Wevtapi.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# EvtOpenChannelConfig function


## -description


Gets a handle that you use to read or modify a channel's configuration property.


## -parameters




### -param Session [in]

A remote session handle that the <a href="https://msdn.microsoft.com/26f1745c-dcca-4452-872e-1fffe20f049c">EvtOpenSession</a> function returns. Set to <b>NULL</b> to access a channel on the local computer.


### -param ChannelPath [in]

The name of the channel to access.


### -param Flags [in]

Reserved. Must be zero.


## -returns



If successful, the function returns a handle to the channel's configuration; otherwise, <b>NULL</b>. If <b>NULL</b>, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function to get the error code.




## -remarks



To get a configuration property, call the <a href="https://msdn.microsoft.com/0f84f51c-716e-4a70-b31c-2b4f40b3fd83">EvtGetChannelConfigProperty</a> function.

To modify a configuration property, call the <a href="https://msdn.microsoft.com/f5f11bd9-5eb0-4afe-8c8b-57fa3850ad56">EvtSetChannelConfigProperty</a> function. To save the configuration changes, call the <a href="https://msdn.microsoft.com/3f3eff67-24b6-448e-bb61-0bc851d9bdfa">EvtSaveChannelConfig</a> function.

To enumerate the registered channels, call the <a href="https://msdn.microsoft.com/eb077b0c-1ae6-40ae-becc-98d840302e6f">EvtOpenChannelEnum</a> function.

You must call the <a href="https://msdn.microsoft.com/c4b82d7b-508d-45bf-b990-04e90e846525">EvtClose</a> function to close the handle when done.


#### Examples

For an example that shows how to use this function, see <a href="https://msdn.microsoft.com/4ee44dae-b390-4d98-bcef-836b53b04860">Getting and Setting a Channel's Configuration Properties</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0f84f51c-716e-4a70-b31c-2b4f40b3fd83">EvtGetChannelConfigProperty</a>



<a href="https://msdn.microsoft.com/eb077b0c-1ae6-40ae-becc-98d840302e6f">EvtOpenChannelEnum</a>



<a href="https://msdn.microsoft.com/3f3eff67-24b6-448e-bb61-0bc851d9bdfa">EvtSaveChannelConfig</a>



<a href="https://msdn.microsoft.com/f5f11bd9-5eb0-4afe-8c8b-57fa3850ad56">EvtSetChannelConfigProperty</a>
 

 

