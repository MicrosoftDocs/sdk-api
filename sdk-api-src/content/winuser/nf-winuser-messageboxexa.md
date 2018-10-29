---
UID: NF:winuser.MessageBoxExA
title: MessageBoxExA function
author: windows-sdk-content
description: Creates, displays, and operates a message box.
old-location: dlgbox\messageboxex.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\messageboxex.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: MessageBoxEx, MessageBoxEx function [Dialog Boxes], MessageBoxExA, MessageBoxExW, _win32_MessageBoxEx, _win32_messageboxex_cpp, dlgbox.messageboxex, winui._win32_messageboxex, winuser/MessageBoxEx, winuser/MessageBoxExA, winuser/MessageBoxExW
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
req.unicode-ansi: MessageBoxExW (Unicode) and MessageBoxExA (ANSI)
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
api_name:
 - MessageBoxEx
 - MessageBoxExA
 - MessageBoxExW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MessageBoxExA function


## -description


Creates, displays, and operates a message box. The message box contains an application-defined message and title, plus any combination of predefined icons and push buttons. The buttons are in the language of the system user interface.
    

Currently <b>MessageBoxEx</b> and <a href="https://msdn.microsoft.com/en-us/library/ms645505(v=VS.85).aspx">MessageBox</a> work the same way.


## -parameters




### -param hWnd [in, optional]

Type: <b>HWND</b>

A handle to the owner window of the message box to be created. If this parameter is <b>NULL</b>, the message box has no owner window. 


### -param lpText [in, optional]

Type: <b>LPCTSTR</b>

The message to be displayed. 


### -param lpCaption [in, optional]

Type: <b>LPCTSTR</b>

The dialog box title. If this parameter is <b>NULL</b>, the default title <b>Error</b> is used. 


### -param uType [in]

Type: <b>UINT</b>

The contents and behavior of the dialog box. For information on the supported flags, see <a href="https://msdn.microsoft.com/en-us/library/ms645505(v=VS.85).aspx">MessageBox</a>.


### -param wLanguageId [in]

Type: <b>WORD</b>

The language for the text displayed in the message box button(s). Specifying a value of zero (0) indicates to display the button text in the default system language. If this parameter is <code>MAKELANGID(LANG_NEUTRAL, SUBLANG_NEUTRAL)</code>, the current language associated with the calling thread is used.
           

To specify a language other than the current language, use the <a href="https://msdn.microsoft.com/cdf6424a-bf2b-4c14-8bc7-8b5f04c29ed3">MAKELANGID</a> macro to create this parameter. For more information, see <b>MAKELANGID</b>.


## -returns



Type: <b>int</b>

If a message box has a <b>Cancel</b> button, the function returns the <b>IDCANCEL</b> value if either the ESC key is pressed or the <b>Cancel</b> button is selected. If the message box has no <b>Cancel</b> button, pressing ESC has no effect. 

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 

If the function succeeds, the return value is one of the following menu-item values.

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



When you use a system-modal message box to indicate that the system is low on memory, the strings pointed to by the <i>lpText</i> and <i>lpCaption</i> parameters should not be taken from a resource file because an attempt to load the resource may fail. 

If you create a message box while a dialog box is present, use a handle to the dialog box as the <i>hWnd</i> parameter. The <i>hWnd</i> parameter should not identify a child window, such as a control in a dialog box. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632588(v=VS.85).aspx">Dialog Boxes</a>



<a href="https://msdn.microsoft.com/cdf6424a-bf2b-4c14-8bc7-8b5f04c29ed3">MAKELANGID</a>



<a href="https://msdn.microsoft.com/70681472-36a5-4ae3-b769-0421cf97ff2a">MessageBeep</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645505(v=VS.85).aspx">MessageBox</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645511(v=VS.85).aspx">MessageBoxIndirect</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633539(v=VS.85).aspx">SetForegroundWindow</a>
 

 

