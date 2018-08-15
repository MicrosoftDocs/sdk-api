---
UID: NF:wtsapi32.WTSVirtualChannelOpen
title: WTSVirtualChannelOpen function
author: windows-sdk-content
description: Opens a handle to the server end of a specified virtual channel.
old-location: termserv\wtsvirtualchannelopen.htm
old-project: termserv
ms.assetid: 0daaf06f-ba05-469c-b888-3df5d9495364
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WTSVirtualChannelOpen, WTSVirtualChannelOpen function [Remote Desktop Services], _win32_wtsvirtualchannelopen, termserv.wtsvirtualchannelopen, wtsapi32/WTSVirtualChannelOpen
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wtsapi32.h
req.include-header: 
req.redist: 
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
 - WTSVirtualChannelOpen
product: Windows
targetos: Windows
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WTSVirtualChannelOpen function


## -description


Opens a handle to the server end of a specified virtual channel.

This function is obsolete. Instead, use the <a href="https://msdn.microsoft.com/5694c4b6-3d0f-4a48-8d15-1e404cbb6164">WTSVirtualChannelOpenEx</a> function.


## -parameters




### -param hServer [in]

This parameter must be WTS_CURRENT_SERVER_HANDLE.


### -param SessionId [in]

A Remote Desktop Services session identifier. To indicate the current session, specify <b>WTS_CURRENT_SESSION</b>. You can use the 
<a href="https://msdn.microsoft.com/6f9dd7d4-48dc-411c-85f1-cd1239d1e106">WTSEnumerateSessions</a> function to retrieve the identifiers of all sessions on a specified RD Session Host server.

To open a virtual channel on another user's session, you need to have permission from the Virtual Channel. For more information, see 
<a href="https://msdn.microsoft.com/448a7f9b-bf12-48eb-a3e7-4512ec288d95">Remote Desktop Services Permissions</a>. To modify permissions on a session, use the Remote Desktop Services Configuration administrative tool.


### -param pVirtualName [in]

A pointer to a <b>null</b>-terminated string containing the virtual channel name. Note that this is an ANSI string even when UNICODE is defined. The virtual channel name consists of one to CHANNEL_NAME_LEN characters, not including the terminating <b>null</b>.


## -returns



If the function succeeds, the return value is a handle to the specified virtual channel.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



When you have finished using the handle, release it by calling the <a href="https://msdn.microsoft.com/d82cb1cd-a9bd-45e8-8a86-2c7dd860b987">WTSVirtualChannelClose</a> function.

For an example that shows how to gain access to a virtual channel file handle that can be used for asynchronous I/O, see 
<a href="https://msdn.microsoft.com/68ae8174-d72b-4b1c-b8e9-ae5fed51d385">WTSVirtualChannelQuery</a>.

If you try to use this function to open the same virtual channel multiple times, it can cause a 10-second delay and disrupt the established channel.




## -see-also




<a href="https://msdn.microsoft.com/6f9dd7d4-48dc-411c-85f1-cd1239d1e106">WTSEnumerateSessions</a>



<a href="https://msdn.microsoft.com/f0b7dce7-59eb-41b8-9a61-65a69d1cc1f3">WTSOpenServer</a>



<a href="https://msdn.microsoft.com/d82cb1cd-a9bd-45e8-8a86-2c7dd860b987">WTSVirtualChannelClose</a>
 

 

