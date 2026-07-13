---
UID: NF:winnetwk.WNetDisconnectDialog1W
title: WNetDisconnectDialog1W function (winnetwk.h)
description: The WNetDisconnectDialog1 function attempts to disconnect a network resource. (Unicode)
helpviewer_keywords: ["WNetDisconnectDialog1", "WNetDisconnectDialog1 function [Windows Networking (WNet)]", "WNetDisconnectDialog1W", "_win32_wnetdisconnectdialog1", "winnetwk/WNetDisconnectDialog1", "winnetwk/WNetDisconnectDialog1W", "wnet.wnetdisconnectdialog1"]
old-location: wnet\wnetdisconnectdialog1.htm
tech.root: WNet
ms.assetid: ec3abf0c-2a18-4d7d-aac4-e086d00fa6fe
ms.date: 12/05/2018
ms.keywords: WNetDisconnectDialog1, WNetDisconnectDialog1 function [Windows Networking (WNet)], WNetDisconnectDialog1A, WNetDisconnectDialog1W, _win32_wnetdisconnectdialog1, winnetwk/WNetDisconnectDialog1, winnetwk/WNetDisconnectDialog1A, winnetwk/WNetDisconnectDialog1W, wnet.wnetdisconnectdialog1
req.header: winnetwk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WNetDisconnectDialog1W (Unicode) and WNetDisconnectDialog1A (ANSI)
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
 - WNetDisconnectDialog1W
 - winnetwk/WNetDisconnectDialog1W
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
 - WNetDisconnectDialog1
 - WNetDisconnectDialog1A
 - WNetDisconnectDialog1W
---

# WNetDisconnectDialog1W function


## -description

The
				<b>WNetDisconnectDialog1</b> function attempts to disconnect a network resource. If the underlying network returns ERROR_OPEN_FILES, the function prompts the user for confirmation. If there is any error, the function informs the user. The function requires a 
<a href="/windows/desktop/api/winnetwk/ns-winnetwk-discdlgstructa">DISCDLGSTRUCT</a> to specify the parameters for the disconnect attempt.

## -parameters

### -param lpConnDlgStruct [in]

Pointer to a 
<b>DISCDLGSTRUCT</b> structure. The structure specifies the behavior for the disconnect attempt.

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
<dt><b>ERROR_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
When the system prompted the user for a decision about disconnecting, the user elected not to disconnect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OPEN_FILES</b></dt>
</dl>
</td>
<td width="60%">
Unable to disconnect because the user is actively using the connection.

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
There is insufficient memory to start the dialog box.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_EXTENDED_ERROR</b></dt>
</dl>
</td>
<td width="60%">
A network-specific error occurred. Call the 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetlasterrora">WNetGetLastError</a> function to obtain a description of the error.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winnetwk/ns-winnetwk-discdlgstructa">DISCDLGSTRUCT</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetconnectiondialog">WNetConnectionDialog</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a">WNetConnectionDialog1</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetdisconnectdialog">WNetDisconnectDialog</a>



<a href="/windows/desktop/WNet/windows-networking-wnet-">Windows
		  Networking (WNet) Overview</a>



<a href="/windows/desktop/WNet/windows-networking-functions">Windows
		  Networking Functions</a>

## -remarks

> [!NOTE]
> The winnetwk.h header defines WNetDisconnectDialog1 as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
