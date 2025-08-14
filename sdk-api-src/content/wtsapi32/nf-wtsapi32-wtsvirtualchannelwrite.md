---
UID: NF:wtsapi32.WTSVirtualChannelWrite
title: WTSVirtualChannelWrite function (wtsapi32.h)
description: Writes data to the server end of a virtual channel.
helpviewer_keywords: ["WTSVirtualChannelWrite","WTSVirtualChannelWrite function [Remote Desktop Services]","_win32_wtsvirtualchannelwrite","termserv.wtsvirtualchannelwrite","wtsapi32/WTSVirtualChannelWrite"]
old-location: termserv\wtsvirtualchannelwrite.htm
tech.root: TermServ
ms.assetid: cb999de8-74a1-4491-bffb-dc4d74a1fea3
ms.date: 12/05/2018
ms.keywords: WTSVirtualChannelWrite, WTSVirtualChannelWrite function [Remote Desktop Services], _win32_wtsvirtualchannelwrite, termserv.wtsvirtualchannelwrite, wtsapi32/WTSVirtualChannelWrite
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
req.dll: Wtsapi32.Dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WTSVirtualChannelWrite
 - wtsapi32/WTSVirtualChannelWrite
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-session-wtsapi32-l1-1-1.dll
 - Wtsapi32.Dll
api_name:
 - WTSVirtualChannelWrite
---

# WTSVirtualChannelWrite function


## -description

Writes 
    data to the server end of a virtual channel.

## -parameters

### -param hChannelHandle [in]

Handle to a virtual channel opened by the 
      <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsvirtualchannelopen">WTSVirtualChannelOpen</a> function.

### -param Buffer [in]

Pointer to a buffer containing the data to write to the virtual channel.

### -param Length [in]

Specifies the size, in bytes, of the data to write.

### -param pBytesWritten [out]

Pointer to a variable that receives the number of bytes written.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<div class="alert"><b>Note</b>  <b>WTSVirtualChannelWrite</b> is not thread safe. 
    To access a virtual channel from multiple threads, or to do asynchronous IO through a virtual channel, use 
    <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsvirtualchannelquery">WTSVirtualChannelQuery</a> with 
    <b>WTSVirtualFileHandle</b>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsvirtualchannelquery">WTSVirtualChannelQuery</a>



<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsvirtualchannelread">WTSVirtualChannelRead</a>