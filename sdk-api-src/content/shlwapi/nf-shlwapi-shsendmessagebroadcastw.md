---
UID: NF:shlwapi.SHSendMessageBroadcastW
title: SHSendMessageBroadcastW function (shlwapi.h)
description: Sends a message to all top-level windows in the system. (Unicode)
helpviewer_keywords: ["SHSendMessageBroadcast", "SHSendMessageBroadcast function [Windows Shell]", "SHSendMessageBroadcastW", "_shell_SHSendMessageBroadcast", "shell.SHSendMessageBroadcast", "shlwapi/SHSendMessageBroadcast", "shlwapi/SHSendMessageBroadcastW"]
old-location: shell\SHSendMessageBroadcast.htm
tech.root: shell
ms.assetid: 98671f0f-2386-486f-ac96-14dd44c776c6
ms.date: 12/05/2018
ms.keywords: SHSendMessageBroadcast, SHSendMessageBroadcast function [Windows Shell], SHSendMessageBroadcastA, SHSendMessageBroadcastW, _shell_SHSendMessageBroadcast, shell.SHSendMessageBroadcast, shlwapi/SHSendMessageBroadcast, shlwapi/SHSendMessageBroadcastA, shlwapi/SHSendMessageBroadcastW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHSendMessageBroadcastW (Unicode) and SHSendMessageBroadcastA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHSendMessageBroadcastW
 - shlwapi/SHSendMessageBroadcastW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shlwapi-l1-2-1.dll
 - ext-ms-win-shell-shlwapi-l1-2-0.dll
 - Shlwapi.dll
 - API-MS-Win-shlwapi-Winrt-storage-l1-1-0.dll
 - api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
 - SHSendMessageBroadcast
 - SHSendMessageBroadcastA
 - SHSendMessageBroadcastW
---

# SHSendMessageBroadcastW function


## -description

<p class="CCE_Message">[This function is available through Windows XP and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Sends a message to all top-level windows in the system.

## -parameters

### -param uMsg [in]

Type: <b>UINT</b>

The message to send.

### -param wParam [in]

Type: <b>WPARAM</b>

Additional message-specific information.

### -param lParam [in]

Type: <b>LPARAM</b>

Additional message-specific information.

## -returns

Type: <b>LRESULT</b>

The return value is not meaningful.

## -remarks

<b>SHSendMessageBroadcast</b> is equivalent to <a href="/windows/desktop/api/winuser/nf-winuser-sendmessage">SendMessage</a> with <b>HWND_BROADCAST</b>. To avoid causing the Shell to become unresponsive in the case where there could be a window in the system that is not responding to messages, use <b>SHSendMessageBroadcast</b>.

<b>SHSendMessageBroadcast</b> is not exported by name. <b>SHSendMessageBroadcastA</b> is exported from Shlwapi.dll as ordinal 432. <b>SHSendMessageBroadcastW</b> is exported from Shlwapi.dll as ordinal 433.




> [!NOTE]
> The shlwapi.h header defines SHSendMessageBroadcast as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
