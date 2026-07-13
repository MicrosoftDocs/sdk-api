---
UID: NF:shlobj.SoftwareUpdateMessageBox
title: SoftwareUpdateMessageBox function (shlobj.h)
description: Displays a standard message box that can be used to notify a user that an application has been updated.
helpviewer_keywords: ["SoftwareUpdateMessageBox","SoftwareUpdateMessageBox function [Windows Shell]","_win32_SoftwareUpdateMessageBox","shell.SoftwareUpdateMessageBox","shlobj/SoftwareUpdateMessageBox"]
old-location: shell\SoftwareUpdateMessageBox.htm
tech.root: shell
ms.assetid: 8b392355-6882-45e3-b915-5091c9ba51ad
ms.date: 12/05/2018
ms.keywords: SoftwareUpdateMessageBox, SoftwareUpdateMessageBox function [Windows Shell], _win32_SoftwareUpdateMessageBox, shell.SoftwareUpdateMessageBox, shlobj/SoftwareUpdateMessageBox
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.lib: shdocvw.lib
req.dll: Shdocvw.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SoftwareUpdateMessageBox
 - shlobj/SoftwareUpdateMessageBox
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shdocvw.dll
api_name:
 - SoftwareUpdateMessageBox
---

# SoftwareUpdateMessageBox function


## -description

Displays a standard message box that can be used to notify a user that an application has been updated.

## -parameters

### -param hWnd [in, optional]

Type: <b>HWND</b>

A handle to the parent window.

### -param pszDistUnit [in]

Type: <b>PCWSTR</b>

The string value containing the identifier for the code distribution unit. For ActiveX controls, <i>pszDistUnit</i> is typically a GUID.

### -param dwFlags

Type: <b>DWORD</b>

Reserved. Must be set to zero.

### -param psdi [out, optional]

Type: <b>LPSOFTDISTINFO</b>

A pointer to a <a href="/windows/desktop/api/urlmon/ns-urlmon-softdistinfo">SOFTDISTINFO</a> structure that, when this method returns successfully, receives the update information. The <b>cbSize</b> member must be initialized to the <code>sizeof(SOFTDISTINFO)</code>.

## -returns

Type: <b>DWORD</b>

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IDNO</b></dt>
</dl>
</td>
<td width="60%">
The user clicked the <b>Do Not Update</b> button on the dialog box.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IDYES</b></dt>
</dl>
</td>
<td width="60%">
The user clicked the <b>Update Now</b> or <b>About Update</b> button. The application should navigate to the HTML page referred to by the <b>szHREF</b> member of the structure pointed to by <i>psdi</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IDIGNORE</b></dt>
</dl>
</td>
<td width="60%">
There is no pending software update.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IDABORT</b></dt>
</dl>
</td>
<td width="60%">
An error occurred.

</td>
</tr>
</table>

## -remarks

The preferred way to handle updates is to author a Channel Definition Format (CDF) with an Open Software Description (OSD) vocabulary and make the shortcut OSD-aware. Refer to the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768023(v=vs.85)">Channel Definition Format</a> documentation for details.

The <b>SoftwareUpdateMessageBox</b> function is intended to be used in the case where Shell shortcut hooks do not work. One example is an application that was not installed on the start menu. If that application needs to do its own software update check, it should use this function.