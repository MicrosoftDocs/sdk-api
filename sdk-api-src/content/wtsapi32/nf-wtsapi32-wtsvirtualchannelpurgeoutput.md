---
UID: NF:wtsapi32.WTSVirtualChannelPurgeOutput
title: WTSVirtualChannelPurgeOutput function
author: windows-driver-content
description: Deletes all queued output data sent from the server to the client on a specified virtual channel.
old-location: termserv\wtsvirtualchannelpurgeoutput.htm
old-project: TermServ
ms.assetid: 9edd06d1-3f5a-4d83-8c3c-16b761ce4c60
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: WTSVirtualChannelPurgeOutput, WTSVirtualChannelPurgeOutput function [Remote Desktop Services], _win32_wtsvirtualchannelpurgeoutput, termserv.wtsvirtualchannelpurgeoutput, wtsapi32/WTSVirtualChannelPurgeOutput
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WTS_VIRTUAL_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wtsapi32.dll
api_name:
-	WTSVirtualChannelPurgeOutput
product: Windows
targetos: Windows
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WTSVirtualChannelPurgeOutput function


## -description


Deletes all queued output data sent from the server to the client on a specified virtual channel.<div class="alert"><b>Note</b>  This function  currently is not used by   Remote Desktop Services.</div>
<div> </div>



## -parameters




### -param hChannelHandle [in]

Handle to a virtual channel opened by the 
<a href="https://msdn.microsoft.com/0daaf06f-ba05-469c-b888-3df5d9495364">WTSVirtualChannelOpen</a> function.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/ec8ee90d-0871-466c-8da3-04813319216a">WTSVirtualChannelPurgeInput</a>
 

 

