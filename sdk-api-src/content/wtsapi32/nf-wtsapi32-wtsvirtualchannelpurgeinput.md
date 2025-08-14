---
UID: NF:wtsapi32.WTSVirtualChannelPurgeInput
title: WTSVirtualChannelPurgeInput function (wtsapi32.h)
description: Deletes all queued input data sent from the client to the server on a specified virtual channel.
helpviewer_keywords: ["WTSVirtualChannelPurgeInput","WTSVirtualChannelPurgeInput function [Remote Desktop Services]","_win32_wtsvirtualchannelpurgeinput","termserv.wtsvirtualchannelpurgeinput","wtsapi32/WTSVirtualChannelPurgeInput"]
old-location: termserv\wtsvirtualchannelpurgeinput.htm
tech.root: TermServ
ms.assetid: ec8ee90d-0871-466c-8da3-04813319216a
ms.date: 12/05/2018
ms.keywords: WTSVirtualChannelPurgeInput, WTSVirtualChannelPurgeInput function [Remote Desktop Services], _win32_wtsvirtualchannelpurgeinput, termserv.wtsvirtualchannelpurgeinput, wtsapi32/WTSVirtualChannelPurgeInput
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
 - WTSVirtualChannelPurgeInput
 - wtsapi32/WTSVirtualChannelPurgeInput
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
 - WTSVirtualChannelPurgeInput
---

# WTSVirtualChannelPurgeInput function


## -description

Deletes all queued input data sent from the client to the server on a specified virtual channel.<div class="alert"><b>Note</b>  This function currently is not used by Remote Desktop Services.</div>
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

<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput">WTSVirtualChannelPurgeOutput</a>