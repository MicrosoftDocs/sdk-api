---
UID: NF:wtsapi32.WTSVirtualChannelClose
title: WTSVirtualChannelClose function
author: windows-sdk-content
description: Closes an open virtual channel handle.
old-location: termserv\wtsvirtualchannelclose.htm
old-project: termserv
ms.assetid: d82cb1cd-a9bd-45e8-8a86-2c7dd860b987
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: WTSVirtualChannelClose, WTSVirtualChannelClose function [Remote Desktop Services], _win32_wtsvirtualchannelclose, termserv.wtsvirtualchannelclose, wtsapi32/WTSVirtualChannelClose
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WTS_VIRTUAL_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wtsapi32.dll
 - Ext-MS-Win-Session-WtsApi32-l1-1-0.dll
api_name:
 - WTSVirtualChannelClose
product: Windows
targetos: Windows
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WTSVirtualChannelClose function


## -description


Closes an open virtual channel handle.


## -parameters




### -param hChannelHandle [in]

Handle to a virtual channel opened by the 
<a href="https://msdn.microsoft.com/0daaf06f-ba05-469c-b888-3df5d9495364">WTSVirtualChannelOpen</a> function.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/0daaf06f-ba05-469c-b888-3df5d9495364">WTSVirtualChannelOpen</a>
 

 

