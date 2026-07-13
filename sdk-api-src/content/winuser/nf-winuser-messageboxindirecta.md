---
UID: NF:winuser.MessageBoxIndirectA
title: MessageBoxIndirectA function (winuser.h)
description: Creates, displays, and operates a message box. The message box contains application-defined message text and title, any icon, and any combination of predefined push buttons. (ANSI)
helpviewer_keywords: ["MessageBoxIndirectA", "winuser/MessageBoxIndirectA"]
old-location: dlgbox\messageboxindirect.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\messageboxindirect.htm
ms.date: 12/05/2018
ms.keywords: MessageBoxIndirect, MessageBoxIndirect function [Dialog Boxes], MessageBoxIndirectA, MessageBoxIndirectW, _win32_MessageBoxIndirect, _win32_messageboxindirect_cpp, dlgbox.messageboxindirect, winui._win32_messageboxindirect, winuser/MessageBoxIndirect, winuser/MessageBoxIndirectA, winuser/MessageBoxIndirectW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MessageBoxIndirectW (Unicode) and MessageBoxIndirectA (ANSI)
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
 - MessageBoxIndirectA
 - winuser/MessageBoxIndirectA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-DialogBox-l1-1-0.dll
 - Ext-MS-Win-NTUser-DialogBox-l1-1-1.dll
 - ext-ms-win-ntuser-dialogbox-l1-1-2.dll
api_name:
 - MessageBoxIndirect
 - MessageBoxIndirectA
 - MessageBoxIndirectW
req.apiset: ext-ms-win-ntuser-dialogbox-l1-1-0 (introduced in Windows 8)
---

# MessageBoxIndirectA function


## -description

Creates, displays, and operates a message box. The message box contains application-defined message text and title, any icon, and any combination of predefined push buttons.

## -parameters

### -param lpmbp [in]

Type: <b>const LPMSGBOXPARAMS</b>

A pointer to a <a href="/windows/desktop/api/winuser/ns-winuser-msgboxparamsa">MSGBOXPARAMS</a> structure that contains information used to display the message box.

## -returns

Type: <b>int</b>

If the function succeeds, the return value is one of the following menu-item values.

If a message box has a <b>Cancel</b> button, the function returns the <b>IDCANCEL</b> value if either the ESC key is pressed or the <b>Cancel</b> button is selected. If the message box has no <b>Cancel</b> button, pressing ESC has no effect. 

If there is not enough memory to create the message box, the return value is zero. 

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IDABORT</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The <b>Abort</b> button was selected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IDCANCEL</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The <b>Cancel</b> button was selected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IDCONTINUE</b></dt>
<dt>11</dt>
</dl>
</td>
<td width="60%">
The <b>Continue</b> button was selected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IDIGNORE</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The <b>Ignore</b> button was selected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IDNO</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
The <b>No</b> button was selected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IDOK</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The <b>OK</b> button was selected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IDRETRY</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The <b>Retry</b> button was selected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IDTRYAGAIN</b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
The <b>Try Again</b> button was selected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IDYES</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The <b>Yes</b> button was selected.

</td>
</tr>
</table>

## -remarks

When you use a system-modal message box to indicate that the system is low on memory, the strings pointed to by the <b>lpszText</b> and <b>lpszCaption</b> members of the <a href="/windows/desktop/api/winuser/ns-winuser-msgboxparamsa">MSGBOXPARAMS</a> structure should not be taken from a resource file, because an attempt to load the resource may fail. 

If you create a message box while a dialog box is present, use a handle to the dialog box as the <i>hWnd</i> parameter. The <i>hWnd</i> parameter should not identify a child window, such as a control in a dialog box. 





> [!NOTE]
> The winuser.h header defines MessageBoxIndirect as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/dlgbox/dialog-boxes">Dialog Boxes</a>



<a href="/windows/desktop/api/winuser/ns-winuser-msgboxparamsa">MSGBOXPARAMS</a>



<a href="/windows/desktop/api/winuser/nf-winuser-messagebox">MessageBox</a>



<a href="/windows/desktop/api/winuser/nf-winuser-messageboxexa">MessageBoxEx</a>



<b>Reference</b>
