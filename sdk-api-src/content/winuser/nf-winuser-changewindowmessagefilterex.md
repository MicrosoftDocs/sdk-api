---
UID: NF:winuser.ChangeWindowMessageFilterEx
title: ChangeWindowMessageFilterEx function (winuser.h)
description: Modifies the User Interface Privilege Isolation (UIPI) message filter for a specified window.
helpviewer_keywords: ["ChangeWindowMessageFilterEx","ChangeWindowMessageFilterEx function [Windows and Messages]","MSGFLT_ALLOW","MSGFLT_DISALLOW","MSGFLT_RESET","_win32_ChangeWindowMessageFilterEx","_win32_changewindowmessagefilterex_cpp","winmsg.changewindowmessagefilterex","winui._win32_changewindowmessagefilterex","winuser/ChangeWindowMessageFilterEx"]
old-location: winmsg\changewindowmessagefilterex.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\changewindowmessagefilterex.htm
ms.date: 12/05/2018
ms.keywords: ChangeWindowMessageFilterEx, ChangeWindowMessageFilterEx function [Windows and Messages], MSGFLT_ALLOW, MSGFLT_DISALLOW, MSGFLT_RESET, _win32_ChangeWindowMessageFilterEx, _win32_changewindowmessagefilterex_cpp, winmsg.changewindowmessagefilterex, winui._win32_changewindowmessagefilterex, winuser/ChangeWindowMessageFilterEx
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ChangeWindowMessageFilterEx
 - winuser/ChangeWindowMessageFilterEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-iam-l1-1-2.dll
 - ext-ms-win-ntuser-gui-l1-3-1.dll
 - User32.dll
 - Ext-MS-Win-RTCore-NTUser-iam-l1-1-0.dll
 - ext-ms-win-ntuser-gui-l1-1-0.dll
 - ext-ms-win-ntuser-gui-l1-1-1.dll
 - ext-ms-win-ntuser-gui-l1-2-0.dll
 - ext-ms-win-ntuser-gui-l1-2-1.dll
 - Ext-MS-Win-NTUser-Gui-L1-3-0.dll
 - Ext-MS-Win-RTCore-NTUser-Iam-L1-1-1.dll
api_name:
 - ChangeWindowMessageFilterEx
req.apiset: ext-ms-win-ntuser-gui-l1-3-0 (introduced in Windows 10, version 10.0.10240)
---

# ChangeWindowMessageFilterEx function


## -description

Modifies the User Interface Privilege Isolation (UIPI) message filter for a specified window.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

A handle to the window whose UIPI message filter is to be modified.

### -param message [in]

Type: <b>UINT</b>

The message that the message filter allows through or blocks.

### -param action [in]

Type: <b>DWORD</b>

The action to be performed, and can take one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSGFLT_ALLOW"></a><a id="msgflt_allow"></a><dl>
<dt><b>MSGFLT_ALLOW</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Allows the message through the filter. This enables the message to be received by 
					<i>hWnd</i>, regardless of the source of the message, 
					even it comes from a lower privileged process.
					

</td>
</tr>
<tr>
<td width="40%"><a id="MSGFLT_DISALLOW"></a><a id="msgflt_disallow"></a><dl>
<dt><b>MSGFLT_DISALLOW</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Blocks the message to be delivered to <i>hWnd</i> if it comes from a lower privileged process, 
					unless the message is allowed process-wide by using the <a href="/windows/desktop/api/winuser/nf-winuser-changewindowmessagefilter">ChangeWindowMessageFilter</a> function 
					or globally.
					

</td>
</tr>
<tr>
<td width="40%"><a id="MSGFLT_RESET"></a><a id="msgflt_reset"></a><dl>
<dt><b>MSGFLT_RESET</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Resets the window message filter for <i>hWnd</i> to the default.   Any message allowed
					globally or process-wide will get through, but any message not included 
					in those two categories, and which comes from a lower privileged process, will be blocked.
					

</td>
</tr>
</table>

### -param pChangeFilterStruct [in, out, optional]

Type: <b>PCHANGEFILTERSTRUCT</b>

Optional pointer to a <a href="/windows/desktop/api/winuser/ns-winuser-changefilterstruct">CHANGEFILTERSTRUCT</a> structure.

## -returns

Type: <b>BOOL</b>

If the function succeeds, it returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

UIPI is a security feature that prevents messages from being received from a lower-integrity-level sender.
		You can use this function to allow specific messages to be delivered to a window even 
		if the message originates from a process at a lower integrity level. Unlike the <a href="/windows/desktop/api/winuser/nf-winuser-changewindowmessagefilter">ChangeWindowMessageFilter</a> function, 
		which controls the process message filter, the <b>ChangeWindowMessageFilterEx</b> function controls the window message filter. 
		

An application may use the <a href="/windows/desktop/api/winuser/nf-winuser-changewindowmessagefilter">ChangeWindowMessageFilter</a> function to 
		allow or block a message in a process-wide manner. 
		If the message is allowed by either the process message filter 
		or the window message filter, it will be delivered to the window.
		

Note that processes at or below <b>SECURITY_MANDATORY_LOW_RID</b> are not allowed to change the message filter. 
		If those processes call this function, it will fail and generate the extended error code, <b>ERROR_ACCESS_DENIED</b>.
		

Certain messages whose value is smaller than <b>WM_USER</b> are required to be passed through the filter, 
		regardless of the filter setting. There will be no effect when you attempt to use this function to 
		allow or block such messages.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-changewindowmessagefilter">ChangeWindowMessageFilter</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="/windows/desktop/winmsg/windows">Windows</a>
