---
UID: NF:winuser.DefDlgProcA
tech.root: dlgbox 
title: DefDlgProcA
ms.date: 04/14/2021
targetos: Windows
description: Calls the default dialog box window procedure to provide default processing for any window messages that a dialog box with a private window class does not process. (ANSI)
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: User32.dll 
req.header: winuser.h
req.idl: 
req.include-header: Windows.h 
req.irql: 
req.kmdf-ver: 
req.lib: User32.lib 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only] 
req.target-min-winversvr: Windows 2000 Server [desktop apps only] 
req.target-type: Windows 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-dialogbox-l1-1-2.dll
 - ext-ms-win-ntuser-dialogbox-l1-1-1.dll
 - ext-ms-win-ntuser-dialogbox-l1-1-0.dll
 - User32.dll
api_name:
 - DefDlgProcA
 - DefDlgProc
f1_keywords:
 - DefDlgProcA
 - winuser/DefDlgProcA
 - DefDlgProc
 - winuser/DefDlgProc
dev_langs:
 - c++
---

# DefDlgProcA function

## -description

Calls the default dialog box window procedure to provide default processing for any window messages that a dialog box with a private window class does not process.

## -parameters

### -param hDlg [in]

Type: <b>HWND</b>

A handle to the dialog box.

### -param Msg [in]

Type: <b>UINT</b>

The message.

### -param wParam [in]

Type: <b>WPARAM</b>

Additional message-specific information.

### -param lParam [in]

Type: <b>LPARAM</b>

Additional message-specific information.

## -returns

Type: <b>LRESULT</b>

The return value specifies the result of the message processing and depends on the message sent.

## -remarks

The <b>DefDlgProc</b> function is the window procedure for the predefined class of dialog box. This procedure provides internal processing for the dialog box by forwarding messages to the dialog box procedure and carrying out default processing for any messages that the dialog box procedure returns as <b>FALSE</b>. Applications that create custom window procedures for their custom dialog boxes often use <b>DefDlgProc</b> instead of the <a href="/windows/desktop/api/winuser/nf-winuser-defwindowproca">DefWindowProc</a> function to carry out default message processing.

Applications create custom dialog box classes by filling a <a href="/windows/desktop/api/winuser/ns-winuser-wndclassa">WNDCLASS</a> structure with appropriate information and registering the class with the <a href="/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a> function. Some applications fill the structure by using the <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoa">GetClassInfo</a> function, specifying the name of the predefined dialog box. In such cases, the applications modify at least the <b>lpszClassName</b> member before registering. In all cases, the <b>cbWndExtra</b> member of <b>WNDCLASS</b> for a custom dialog box class must be set to at least <b>DLGWINDOWEXTRA</b>.

The <b>DefDlgProc</b> function must not be called by a dialog box procedure; doing so results in recursive execution.

## -see-also

<b>Conceptual</b>  

<a href="/windows/desktop/api/winuser/nf-winuser-defwindowproca">DefWindowProc</a>  
<a href="/windows/desktop/dlgbox/dialog-boxes">Dialog Boxes</a>  
<a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoa">GetClassInfo</a>  

<b>Reference</b>

<a href="/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a>  
<a href="/windows/desktop/api/winuser/ns-winuser-wndclassa">WNDCLASS</a>  
