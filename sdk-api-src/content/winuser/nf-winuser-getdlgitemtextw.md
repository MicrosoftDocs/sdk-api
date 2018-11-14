---
UID: NF:winuser.GetDlgItemTextW
title: GetDlgItemTextW function
author: windows-sdk-content
description: Retrieves the title or text associated with a control in a dialog box.
old-location: dlgbox\getdlgitemtext.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\getdlgitemtext.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetDlgItemText, GetDlgItemText function [Dialog Boxes], GetDlgItemTextA, GetDlgItemTextW, _win32_GetDlgItemText, _win32_getdlgitemtext_cpp, dlgbox.getdlgitemtext, winui._win32_getdlgitemtext, winuser/GetDlgItemText, winuser/GetDlgItemTextA, winuser/GetDlgItemTextW
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
- apiref
: 
- 
: 
- GetDlgItemTextW
: 
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

The <b>GetDlgItemText</b> function sends a <a href="https://msdn.microsoft.com/117c3d6d-24cd-462f-bdb0-b65d8914273a">WM_GETTEXT</a> message to the control. 


#### Examples

For an example, see <a href="using_dialog_boxes.htm">Creating a Modal Dialog Box</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/07ebee3c-5aa7-4b0d-b6cb-e642e01e1a88">Dialog Boxes</a>



<a href="https://msdn.microsoft.com/8a0b8275-35e5-4983-9b2d-968023d39aa3">GetDlgItemInt</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8c71aa0e-1287-4a56-bef5-bcdddc9d9332">SetDlgItemInt</a>



<a href="https://msdn.microsoft.com/af359c1c-f3ec-4901-97bb-3fb654f44598">SetDlgItemText</a>



<a href="https://msdn.microsoft.com/117c3d6d-24cd-462f-bdb0-b65d8914273a">WM_GETTEXT</a>
 

 

