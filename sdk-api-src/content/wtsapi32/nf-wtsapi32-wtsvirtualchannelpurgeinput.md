---
UID: NF:wtsapi32.WTSVirtualChannelPurgeInput
title: WTSVirtualChannelPurgeInput function
author: windows-sdk-content
description: Deletes all queued input data sent from the client to the server on a specified virtual channel.
old-location: termserv\wtsvirtualchannelpurgeinput.htm
tech.root: TermServ
ms.assetid: ec8ee90d-0871-466c-8da3-04813319216a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WTSVirtualChannelPurgeInput, WTSVirtualChannelPurgeInput function [Remote Desktop Services], _win32_wtsvirtualchannelpurgeinput, termserv.wtsvirtualchannelpurgeinput, wtsapi32/WTSVirtualChannelPurgeInput
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
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wtsapi32.dll
api_name:
 - WTSVirtualChannelPurgeInput
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WTSVirtualChannelPurgeInput function


## -description


Deletes all queued input data sent from the client to the server on a specified virtual channel.<div class="alert"><b>Note</b>  This function currently is not used by Remote Desktop Services.</div>
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




<a href="https://msdn.microsoft.com/9edd06d1-3f5a-4d83-8c3c-16b761ce4c60">WTSVirtualChannelPurgeOutput</a>
 

 

