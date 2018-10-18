---
UID: NF:winuser.MessageBoxIndirectA
title: MessageBoxIndirectA function
author: windows-sdk-content
description: Creates, displays, and operates a message box. The message box contains application-defined message text and title, any icon, and any combination of predefined push buttons.
old-location: dlgbox\messageboxindirect.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\messageboxindirect.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: MessageBoxIndirect, MessageBoxIndirect function [Dialog Boxes], MessageBoxIndirectA, MessageBoxIndirectW, _win32_MessageBoxIndirect, _win32_messageboxindirect_cpp, dlgbox.messageboxindirect, winui._win32_messageboxindirect, winuser/MessageBoxIndirect, winuser/MessageBoxIndirectA, winuser/MessageBoxIndirectW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MessageBoxIndirectA function


## -description


Creates, displays, and operates a message box. The message box contains application-defined message text and title, any icon, and any combination of predefined push buttons.


## -parameters




### -param lpmbp [in]

Type: <b>const LPMSGBOXPARAMS</b>

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms645402(v=VS.85).aspx">MSGBOXPARAMS</a> structure that contains information used to display the message box. 


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



When you use a system-modal message box to indicate that the system is low on memory, the strings pointed to by the <b>lpszText</b> and <b>lpszCaption</b> members of the <a href="https://msdn.microsoft.com/en-us/library/ms645402(v=VS.85).aspx">MSGBOXPARAMS</a> structure should not be taken from a resource file, because an attempt to load the resource may fail. 

If you create a message box while a dialog box is present, use a handle to the dialog box as the <i>hWnd</i> parameter. The <i>hWnd</i> parameter should not identify a child window, such as a control in a dialog box. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632588(v=VS.85).aspx">Dialog Boxes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645402(v=VS.85).aspx">MSGBOXPARAMS</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645505(v=VS.85).aspx">MessageBox</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645507(v=VS.85).aspx">MessageBoxEx</a>



<b>Reference</b>
 

 

