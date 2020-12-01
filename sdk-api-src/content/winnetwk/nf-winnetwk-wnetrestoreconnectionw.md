---
UID: NF:winnetwk.WNetRestoreConnectionW
title: WNetRestoreConnectionW function (winnetwk.h)
description: The WNetRestoreConnectionW function restores the connection to a network resource. The function prompts the user, if necessary, for a name and password.
helpviewer_keywords: ["WNetRestoreConnectionW","WNetRestoreConnectionW function [Windows Networking (WNet)]","winnetwk/WNetRestoreConnectionW","wnet.wnetrestoreconnectionw"]
old-location: wnet\wnetrestoreconnectionw.htm
tech.root: WNet
ms.assetid: 641b37f1-9cea-4c7a-9b42-b4bd28c747ad
ms.date: 12/05/2018
ms.keywords: WNetRestoreConnectionW, WNetRestoreConnectionW function [Windows Networking (WNet)], winnetwk/WNetRestoreConnectionW, wnet.wnetrestoreconnectionw
req.header: winnetwk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mpr.lib
req.dll: Mpr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WNetRestoreConnectionW
 - winnetwk/WNetRestoreConnectionW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mpr.dll
api_name:
 - WNetRestoreConnectionW
---

# WNetRestoreConnectionW function


## -description

<p class="CCE_Message">[<b>WNetRestoreConnectionW</b> is not available for use as of Windows Vista.]

The <b>WNetRestoreConnectionW</b> function restores the connection to a network resource. The function prompts the user, if necessary, for a name and password.

## -parameters

### -param hWnd [in]

Handle to the parent window that the function uses to display the user interface (UI) that prompts the user for a name and password when making the network connection. If this parameter is <b>NULL</b>, there is no owner window.

### -param lpDevice [in]

Pointer to a <b>null</b>-terminated Unicode string that specifies the local name of the drive to connect to, such as "Z:". If this parameter is <b>NULL</b>, the function reconnects all persistent drives stored in the registry for the current user.


#### - fUseUI

If true, display a username/password prompt to the caller; otherwise, do not display it. The default value is true.

## -returns

If the function succeeds, the return value is NO_ERROR. 

If the function fails, the return value is a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>, such as one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have access to the network resource.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ALREADY_ASSIGNED</b></dt>
</dl>
</td>
<td width="60%">
The local device specified by <i>lpDevice</i> is already connected to a network resource.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_DEV_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The type of local device and the type of network resource do not match.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
The value specified by <i>lpDevice</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_PROFILE</b></dt>
</dl>
</td>
<td width="60%">
The user profile is in an incorrect format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUSY</b></dt>
</dl>
</td>
<td width="60%">
The router or provider is busy, possibly initializing. The caller should retry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The attempt to make the connection was canceled by the user through a dialog box from one of the network resource providers, or by a called resource.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANNOT_OPEN_PROFILE</b></dt>
</dl>
</td>
<td width="60%">
The system is unable to open the user profile to process persistent connections.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DEVICE_ALREADY_REMEMBERED</b></dt>
</dl>
</td>
<td width="60%">
An entry for the device is already in the user profile.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_EXTENDED_ERROR</b></dt>
</dl>
</td>
<td width="60%">
A network-specific error occurred. Call the <a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetlasterrora">WNetGetLastError</a> function to obtain a description of the error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PASSWORD</b></dt>
</dl>
</td>
<td width="60%">
The specified password is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_NET_OR_BAD_PATH</b></dt>
</dl>
</td>
<td width="60%">
The operation cannot be performed because a network component is not started or because a specified name cannot be used.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_NETWORK</b></dt>
</dl>
</td>
<td width="60%">
The network is unavailable.

</td>
</tr>
</table>

## -remarks

The <b>WNetRestoreConnectionW</b> function is not supported on Windows Vista and later. 



To call this function, first call the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> function to load Mpr.dll. Then call the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> function to retrieve the address of the <b>WNetRestoreConnectionW</b> function. 

<b>WNetRestoreConnectionW</b> is used by Winlogon to restore all persistent drive mappings during the interactive logon process. The function is also called by the Microsoft Windows Shell to reconnect individual drives at the user's request. This can occur, for example, when a drive fails to reconnect at logon and the user double-clicks the drive under the My Computer virtual folder.

## -see-also

<a href="/windows/desktop/WNet/windows-networking-wnet-">Windows
			 Networking (WNet) Overview</a>



<a href="/windows/desktop/WNet/windows-networking-functions">Windows
			 Networking Functions</a>