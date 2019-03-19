---
UID: NF:winuser.GetDlgItemTextW
title: GetDlgItemTextW function (winuser.h)
author: windows-sdk-content
description: Retrieves the title or text associated with a control in a dialog box.
old-location: dlgbox\getdlgitemtext.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\getdlgitemtext.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetDlgItemText, GetDlgItemText function [Dialog Boxes], GetDlgItemTextA, GetDlgItemTextW, _win32_GetDlgItemText, _win32_getdlgitemtext_cpp, dlgbox.getdlgitemtext, winui._win32_getdlgitemtext, winuser/GetDlgItemText, winuser/GetDlgItemTextA, winuser/GetDlgItemTextW
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetDlgItemTextW (Unicode) and GetDlgItemTextA (ANSI)
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
 - GetDlgItemText
 - GetDlgItemTextA
 - GetDlgItemTextW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetDlgItemTextW function


## -description


Retrieves the title or text associated with a control in a dialog box. 


## -parameters




### -param hDlg [in]

Type: <b>HWND</b>

A handle to the dialog box that contains the control. 


### -param nIDDlgItem [in]

Type: <b>int</b>

The identifier of the control whose title or text is to be retrieved. 


### -param lpString [out]

Type: <b>LPTSTR</b>

The buffer to receive the title or text. 


### -param cchMax [in]

Type: <b>int</b>

The maximum length, in characters, of the string to be copied to the buffer pointed to by <i>lpString</i>. If the length of the string, including the null character, exceeds the limit, the string is truncated. 


## -returns



Type: <b>UINT</b>

If the function succeeds, the return value specifies the number of characters copied to the buffer, not including the terminating null character.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the string is as long or longer than the buffer, the buffer will contain the truncated string with a terminating null character.

The <b>GetDlgItemText</b> function sends a <a href="https://msdn.microsoft.com/en-us/library/ms632627(v=VS.85).aspx">WM_GETTEXT</a> message to the control. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms644996(v=VS.85).aspx">Creating a Modal Dialog Box</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632588(v=VS.85).aspx">Dialog Boxes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645485(v=VS.85).aspx">GetDlgItemInt</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms645518(v=VS.85).aspx">SetDlgItemInt</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645521(v=VS.85).aspx">SetDlgItemText</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632627(v=VS.85).aspx">WM_GETTEXT</a>
 

 

