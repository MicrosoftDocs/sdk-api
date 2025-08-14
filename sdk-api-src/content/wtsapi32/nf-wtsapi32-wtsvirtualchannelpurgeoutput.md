---
UID: NF:wtsapi32.WTSVirtualChannelPurgeOutput
title: WTSVirtualChannelPurgeOutput function (wtsapi32.h)
description: Deletes all queued output data sent from the server to the client on a specified virtual channel.
helpviewer_keywords: ["WTSVirtualChannelPurgeOutput","WTSVirtualChannelPurgeOutput function [Remote Desktop Services]","_win32_wtsvirtualchannelpurgeoutput","termserv.wtsvirtualchannelpurgeoutput","wtsapi32/WTSVirtualChannelPurgeOutput"]
old-location: termserv\wtsvirtualchannelpurgeoutput.htm
tech.root: TermServ
ms.assetid: 9edd06d1-3f5a-4d83-8c3c-16b761ce4c60
ms.date: 12/05/2018
ms.keywords: WTSVirtualChannelPurgeOutput, WTSVirtualChannelPurgeOutput function [Remote Desktop Services], _win32_wtsvirtualchannelpurgeoutput, termserv.wtsvirtualchannelpurgeoutput, wtsapi32/WTSVirtualChannelPurgeOutput
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
 - WTSVirtualChannelPurgeOutput
 - wtsapi32/WTSVirtualChannelPurgeOutput
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
api_name:
 - WTSVirtualChannelPurgeOutput
---

# WTSVirtualChannelPurgeOutput function


## -description

Deletes all queued output data sent from the server to the client on a specified virtual channel.<div class="alert"><b>Note</b>  This function  currently is not used by   Remote Desktop Services.</div>
<div> </div>

## -parameters

### -param hChannelHandle [in]

Handle to a virtual channel opened by the 
<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsvirtualchannelopen">WTSVirtualChannelOpen</a> function.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput">WTSVirtualChannelPurgeInput</a>