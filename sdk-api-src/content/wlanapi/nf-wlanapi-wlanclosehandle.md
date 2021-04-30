---
UID: NF:wlanapi.WlanCloseHandle
title: WlanCloseHandle function (wlanapi.h)
description: Closes a connection to the server.
helpviewer_keywords: ["WlanCloseHandle","WlanCloseHandle function [NativeWIFI]","nwifi.wlanclosehandle","wlanapi/WlanCloseHandle"]
old-location: nwifi\wlanclosehandle.htm
tech.root: nwifi
ms.assetid: 8e944133-2616-4e17-ac38-c17e8d25ccec
ms.date: 12/05/2018
ms.keywords: WlanCloseHandle, WlanCloseHandle function [NativeWIFI], nwifi.wlanclosehandle, wlanapi/WlanCloseHandle
req.header: wlanapi.h
req.include-header: Wlanapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wlanapi.lib
req.dll: Wlanapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Wireless LAN API for Windows XP with SP2
ms.custom: 19H1
f1_keywords:
 - WlanCloseHandle
 - wlanapi/WlanCloseHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - wlanapi.dll
 - Ext-MS-Win-networking-wlanapi-l1-1-0.dll
api_name:
 - WlanCloseHandle
---

# WlanCloseHandle function


## -description

The <b>WlanCloseHandle</b> function closes a connection to the server.

## -parameters

### -param hClientHandle [in]

The client's session handle, which identifies the connection to be closed. This handle was  obtained by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param pReserved

Reserved for future use.  Set this parameter to <b>NULL</b>.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value may be one of the following return codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
<i>hClientHandle</i> is <b>NULL</b> or invalid, or <i>pReserved</i> is not <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle <i>hClientHandle</i>  was not found in the handle table.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_STATUS</b></dt>
</dl>
</td>
<td width="60%">
Various error codes.

</td>
</tr>
</table>

## -remarks

After a connection has been closed, any attempted use of the closed handle can cause unexpected errors.  Upon closing, all outstanding notifications are discarded.

  Do not call <b>WlanCloseHandle</b> from a callback function. If the client is in the middle of a notification callback when <b>WlanCloseHandle</b> is called, the function waits for the callback to finish before returning a value.  Calling this function inside a callback function will result in the call never completing. If both the callback function and the thread that closes the handle try to acquire the same lock, a deadlock may occur. In addition, do not call <b>WlanCloseHandle</b> from the <b>DllMain</b> function in an application DLL. This could also cause a deadlock.

## -see-also

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a>