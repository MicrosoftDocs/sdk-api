---
UID: NF:wtsapi32.WTSVirtualChannelOpen
title: WTSVirtualChannelOpen function (wtsapi32.h)
description: Opens a handle to the server end of a specified virtual channel.
helpviewer_keywords: ["WTSVirtualChannelOpen","WTSVirtualChannelOpen function [Remote Desktop Services]","_win32_wtsvirtualchannelopen","termserv.wtsvirtualchannelopen","wtsapi32/WTSVirtualChannelOpen"]
old-location: termserv\wtsvirtualchannelopen.htm
tech.root: TermServ
ms.assetid: 0daaf06f-ba05-469c-b888-3df5d9495364
ms.date: 12/05/2018
ms.keywords: WTSVirtualChannelOpen, WTSVirtualChannelOpen function [Remote Desktop Services], _win32_wtsvirtualchannelopen, termserv.wtsvirtualchannelopen, wtsapi32/WTSVirtualChannelOpen
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WTSVirtualChannelOpen
 - wtsapi32/WTSVirtualChannelOpen
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-session-wtsapi32-l1-1-1.dll
 - Wtsapi32.dll
 - Ext-MS-Win-Session-WtsApi32-l1-1-0.dll
api_name:
 - WTSVirtualChannelOpen
req.apiset: ext-ms-win-session-wtsapi32-l1-1-0 (introduced in Windows 8)
---

# WTSVirtualChannelOpen function


## -description

Opens a handle to the server end of a specified virtual channel.

This function is obsolete. Instead, use the <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex">WTSVirtualChannelOpenEx</a> function.

## -parameters

### -param hServer [in]

This parameter must be WTS_CURRENT_SERVER_HANDLE.

### -param SessionId [in]

A Remote Desktop Services session identifier. To indicate the current session, specify <b>WTS_CURRENT_SESSION</b>. You can use the 
<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsa">WTSEnumerateSessions</a> function to retrieve the identifiers of all sessions on a specified RD Session Host server.

To open a virtual channel on another user's session, you need to have permission from the Virtual Channel. For more information, see 
<a href="/windows/desktop/TermServ/terminal-services-permissions">Remote Desktop Services Permissions</a>. To modify permissions on a session, use the Remote Desktop Services Configuration administrative tool.

### -param pVirtualName [in]

A pointer to a <b>null</b>-terminated string containing the virtual channel name. Note that this is an ANSI string even when UNICODE is defined. The virtual channel name consists of one to CHANNEL_NAME_LEN characters, not including the terminating <b>null</b>.

## -returns

If the function succeeds, the return value is a handle to the specified virtual channel.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

When you have finished using the handle, release it by calling the <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsvirtualchannelclose">WTSVirtualChannelClose</a> function.

For an example that shows how to gain access to a virtual channel file handle that can be used for asynchronous I/O, see 
<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsvirtualchannelquery">WTSVirtualChannelQuery</a>.

If you try to use this function to open the same virtual channel multiple times, it can cause a 10-second delay and disrupt the established channel.

## -see-also

<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsa">WTSEnumerateSessions</a>



<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenservera">WTSOpenServer</a>



<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsvirtualchannelclose">WTSVirtualChannelClose</a>
