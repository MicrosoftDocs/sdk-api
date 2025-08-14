---
UID: NF:winnetwk.WNetConnectionDialog1W
title: WNetConnectionDialog1W function (winnetwk.h)
description: The WNetConnectionDialog1 function brings up a general browsing dialog for connecting to network resources. The function requires a CONNECTDLGSTRUCT to establish the dialog box parameters. (Unicode)
helpviewer_keywords: ["WNetConnectionDialog1", "WNetConnectionDialog1 function [Windows Networking (WNet)]", "WNetConnectionDialog1W", "_win32_wnetconnectiondialog1", "winnetwk/WNetConnectionDialog1", "winnetwk/WNetConnectionDialog1W", "wnet.wnetconnectiondialog1"]
old-location: wnet\wnetconnectiondialog1.htm
tech.root: WNet
ms.assetid: 11390693-0ab3-4f8b-9209-bc0bceb98032
ms.date: 12/05/2018
ms.keywords: WNetConnectionDialog1, WNetConnectionDialog1 function [Windows Networking (WNet)], WNetConnectionDialog1A, WNetConnectionDialog1W, _win32_wnetconnectiondialog1, winnetwk/WNetConnectionDialog1, winnetwk/WNetConnectionDialog1A, winnetwk/WNetConnectionDialog1W, wnet.wnetconnectiondialog1
req.header: winnetwk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WNetConnectionDialog1W (Unicode) and WNetConnectionDialog1A (ANSI)
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
 - WNetConnectionDialog1W
 - winnetwk/WNetConnectionDialog1W
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
 - WNetConnectionDialog1
 - WNetConnectionDialog1A
 - WNetConnectionDialog1W
---

# WNetConnectionDialog1W function


## -description

The
				<b>WNetConnectionDialog1</b> function brings up a general browsing dialog for connecting to network resources. The function requires a 
<a href="/windows/desktop/api/winnetwk/ns-winnetwk-connectdlgstructa">CONNECTDLGSTRUCT</a> to establish the dialog box parameters.

## -parameters

### -param lpConnDlgStruct [in, out]

Pointer to a 
<b>CONNECTDLGSTRUCT</b> structure. The structure establishes the browsing dialog parameters.

## -returns

If the user cancels the dialog box, the function returns –1. If the function is successful, it returns NO_ERROR. Also, if the call is successful, the <b>dwDevNum</b> member of the 
<b>CONNECTDLGSTRUCT</b> structure contains the number of the connected device.

Typically this dialog returns an error only if the user cannot enter a dialog session. This is because errors that occur after a dialog session are reported to the user directly. If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a>, such as one of the following values.

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
Both the CONNDLG_RO_PATH and the CONNDLG_USE_MRU dialog box options are set. (Dialog box options are specified by the <b>dwFlags</b> member of the 
<a href="/windows/desktop/api/winnetwk/ns-winnetwk-connectdlgstructa">CONNECTDLGSTRUCT</a> structure.) 




-or-

Both the CONNDLG_PERSIST and the CONNDLG_NOT_PERSIST dialog box options are set.

-or-

The CONNDLG_RO_PATH dialog box option is set and the <b>lpRemoteName</b> member of the <a href="ns-winnetwk-netresourcew.md">NETRESOURCE</a> structure does not point to a remote network. (The <b>CONNECTDLGSTRUCT</b> structure points to a <b>NETRESOURCE</b> structure.)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_DEV_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The <b>dwType</b> member of the 
<b>NETRESOURCE</b> structure is not set to RESOURCETYPE_DISK.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUSY</b></dt>
</dl>
</td>
<td width="60%">
The network provider is busy (possibly initializing). The caller should retry.

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
There is insufficient memory to display the dialog box.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_EXTENDED_ERROR</b></dt>
</dl>
</td>
<td width="60%">
A network-specific error occurred. Call 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetlasterrora">WNetGetLastError</a> to obtain a description of the error.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winnetwk/ns-winnetwk-connectdlgstructa">CONNECTDLGSTRUCT</a>



<a href="ns-winnetwk-netresourcew.md">NETRESOURCE</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetconnectiondialog">WNetConnectionDialog</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetdisconnectdialog">WNetDisconnectDialog</a>



<a href="/windows/desktop/WNet/windows-networking-wnet-">Windows
		  Networking (WNet) Overview</a>



<a href="/windows/desktop/WNet/windows-networking-functions">Windows
		  Networking Functions</a>

## -remarks

> [!NOTE]
> The winnetwk.h header defines WNetConnectionDialog1 as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
