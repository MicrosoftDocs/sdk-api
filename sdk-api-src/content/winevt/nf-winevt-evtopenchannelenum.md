---
UID: NF:winevt.EvtOpenChannelEnum
title: EvtOpenChannelEnum function
author: windows-driver-content
description: Gets a handle that you use to enumerate the list of channels that are registered on the computer.
old-location: wes\evtopenchannelenum.htm
old-project: WES
ms.assetid: eb077b0c-1ae6-40ae-becc-98d840302e6f
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: EvtOpenChannelEnum, EvtOpenChannelEnum function [EventLog], wes.evtopenchannelenum, winevt/EvtOpenChannelEnum
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
req.typenames: EVT_VARIANT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wevtapi.dll
api_name:
-	EvtOpenChannelEnum
product: Windows
targetos: Windows
req.lib: Wevtapi.lib
req.dll: Wevtapi.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# EvtOpenChannelEnum function


## -description


Gets a handle that you use to enumerate the list of channels that are registered on the computer.


## -parameters




### -param Session [in]

A remote session handle that the <a href="https://msdn.microsoft.com/26f1745c-dcca-4452-872e-1fffe20f049c">EvtOpenSession</a> function returns. Set to <b>NULL</b> to enumerate the channels on the local computer.


### -param Flags [in]

Reserved. Must be zero.


## -returns



If successful, the function returns a handle to the list of channel names that are registered on the computer; otherwise, <b>NULL</b>. If <b>NULL</b>, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function to get the error code.




## -remarks



The enumeration includes all the channels that the providers that are registered on the computer defined. To enumerate the channel names, call the <a href="https://msdn.microsoft.com/51fd2449-8a89-4a18-99c3-b974c2c998ca">EvtNextChannelPath</a> function in a loop. The names are sorted alphabetically.

You must call the <a href="https://msdn.microsoft.com/c4b82d7b-508d-45bf-b990-04e90e846525">EvtClose</a> function to close the enumerator handle when done.


#### Examples

For an example that shows how to use this function, see <a href="https://msdn.microsoft.com/4ee44dae-b390-4d98-bcef-836b53b04860">Getting and Setting a Channel's Configuration Properties</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/51fd2449-8a89-4a18-99c3-b974c2c998ca">EvtNextChannelPath</a>



<a href="https://msdn.microsoft.com/d197f04e-01e8-4ef6-a9ca-61e5178d825b">EvtOpenChannelConfig</a>
 

 

