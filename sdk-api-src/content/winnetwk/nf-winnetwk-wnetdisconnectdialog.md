---
UID: NF:winnetwk.WNetDisconnectDialog
title: WNetDisconnectDialog function (winnetwk.h)
description: The WNetDisconnectDialog function starts a general browsing dialog box for disconnecting from network resources. The function requires a handle to the owner window for the dialog box.
helpviewer_keywords: ["RESOURCETYPE_DISK","WNetDisconnectDialog","WNetDisconnectDialog function [Windows Networking (WNet)]","_win32_wnetdisconnectdialog","winnetwk/WNetDisconnectDialog","wnet.wnetdisconnectdialog"]
old-location: wnet\wnetdisconnectdialog.htm
tech.root: WNet
ms.assetid: 76e0f38a-e057-4496-9c2f-7ea73d19bd76
ms.date: 12/05/2018
ms.keywords: RESOURCETYPE_DISK, WNetDisconnectDialog, WNetDisconnectDialog function [Windows Networking (WNet)], _win32_wnetdisconnectdialog, winnetwk/WNetDisconnectDialog, wnet.wnetdisconnectdialog
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
 - WNetDisconnectDialog
 - winnetwk/WNetDisconnectDialog
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mpr.dll
 - API-MS-Win-Core-multipleproviderrouter-l1-1-0.dll
api_name:
 - WNetDisconnectDialog
---

# WNetDisconnectDialog function


## -description

The
				<b>WNetDisconnectDialog</b> function starts a general browsing dialog box for disconnecting from network resources. The function requires a handle to the owner window for the dialog box.

## -parameters

### -param hwnd [in]

Handle to the owner window for the dialog box.

### -param dwType [in]

Resource type to disconnect from. This parameter can have the following value. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RESOURCETYPE_DISK"></a><a id="resourcetype_disk"></a><dl>
<dt><b>RESOURCETYPE_DISK</b></dt>
</dl>
</td>
<td width="60%">
Disconnects from disk resources.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is NO_ERROR. If the user cancels the dialog box, the return value is –1.

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a>, such as one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_EXTENDED_ERROR</b></dt>
</dl>
</td>
<td width="60%">
A network-specific error occurred. To obtain a description of the error, call the 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetlasterrora">WNetGetLastError</a> function.

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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory to start the dialog box.

</td>
</tr>
</table>

## -remarks

The 
<b>WNetDisconnectDialog</b> function returns immediately and creates a dialog box for disconnecting networked drives. This dialog box runs asynchronously on a worker thread.

If the worker thread is terminated, the owner window and its associated dialog box are also terminated. If this occurs, the user might not be able to interact with the dialog box, because it will not  appear on the user's screen or will appear briefly.

## -see-also

<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a">WNetAddConnection2</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a">WNetCancelConnection2</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetconnectiondialog">WNetConnectionDialog</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a">WNetConnectionDialog1</a>



<a href="/windows/desktop/WNet/windows-networking-wnet-">Windows
		  Networking (WNet) Overview</a>



<a href="/windows/desktop/WNet/windows-networking-functions">Windows
		  Networking Functions</a>