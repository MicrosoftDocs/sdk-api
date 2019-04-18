---
UID: NF:winuser.SetDlgItemTextW
title: SetDlgItemTextW function (winuser.h)
author: windows-sdk-content
description: Sets the title or text of a control in a dialog box.
old-location: dlgbox\setdlgitemtext.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\setdlgitemtext.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetDlgItemText, SetDlgItemText function [Dialog Boxes], SetDlgItemTextA, SetDlgItemTextW, _win32_SetDlgItemText, _win32_setdlgitemtext_cpp, dlgbox.setdlgitemtext, winui._win32_setdlgitemtext, winuser/SetDlgItemText, winuser/SetDlgItemTextA, winuser/SetDlgItemTextW
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetDlgItemTextW (Unicode) and SetDlgItemTextA (ANSI)
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
 - SetDlgItemText
 - SetDlgItemTextA
 - SetDlgItemTextW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetDlgItemTextW function


## -description


Sets the title or text of a control in a dialog box. 


## -parameters




### -param hDlg [in]

Type: <b>HWND</b>

A handle to the dialog box that contains the control. 


### -param nIDDlgItem [in]

Type: <b>int</b>

The control with a title or text to be set. 


### -param lpString [in]

Type: <b>LPCTSTR</b>

The text to be copied to the control. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The <b>SetDlgItemText</b> function sends a <a href="https://msdn.microsoft.com/en-us/library/ms632644(v=VS.85).aspx">WM_SETTEXT</a> message to the specified control. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/Bb775148(v=VS.85).aspx">Using List Boxes</a>. 

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632588(v=VS.85).aspx">Dialog Boxes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645485(v=VS.85).aspx">GetDlgItemInt</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645489(v=VS.85).aspx">GetDlgItemText</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms645518(v=VS.85).aspx">SetDlgItemInt</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632644(v=VS.85).aspx">WM_SETTEXT</a>
 

 

