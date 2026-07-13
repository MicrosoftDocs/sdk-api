---
UID: NF:wtsapi32.WTSVirtualChannelClose
title: WTSVirtualChannelClose function (wtsapi32.h)
description: Closes an open virtual channel handle.
helpviewer_keywords: ["WTSVirtualChannelClose","WTSVirtualChannelClose function [Remote Desktop Services]","_win32_wtsvirtualchannelclose","termserv.wtsvirtualchannelclose","wtsapi32/WTSVirtualChannelClose"]
old-location: termserv\wtsvirtualchannelclose.htm
tech.root: TermServ
ms.assetid: d82cb1cd-a9bd-45e8-8a86-2c7dd860b987
ms.date: 12/05/2018
ms.keywords: WTSVirtualChannelClose, WTSVirtualChannelClose function [Remote Desktop Services], _win32_wtsvirtualchannelclose, termserv.wtsvirtualchannelclose, wtsapi32/WTSVirtualChannelClose
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
 - WTSVirtualChannelClose
 - wtsapi32/WTSVirtualChannelClose
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
 - WTSVirtualChannelClose
req.apiset: ext-ms-win-session-wtsapi32-l1-1-0 (introduced in Windows 8)
---

# WTSVirtualChannelClose function


## -description

Closes an open virtual channel handle.

## -parameters

### -param hChannelHandle [in]

Handle to a virtual channel opened by the 
<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsvirtualchannelopen">WTSVirtualChannelOpen</a> function.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsvirtualchannelopen">WTSVirtualChannelOpen</a>
