---
UID: NF:winuser.SetDlgItemTextA
title: SetDlgItemTextA function
author: windows-driver-content
description: Sets the title or text of a control in a dialog box.
old-location: dlgbox\setdlgitemtext.htm
old-project: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\setdlgitemtext.htm
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: SetDlgItemText, SetDlgItemText function [Dialog Boxes], SetDlgItemTextA, SetDlgItemTextW, _win32_SetDlgItemText, _win32_setdlgitemtext_cpp, dlgbox.setdlgitemtext, winui._win32_setdlgitemtext, winuser/SetDlgItemText, winuser/SetDlgItemTextA, winuser/SetDlgItemTextW
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
req.unicode-ansi: SetDlgItemTextW (Unicode) and SetDlgItemTextA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AR_STATE, *PAR_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	User32.dll
-	Ext-MS-Win-NTUser-DialogBox-l1-1-0.dll
-	Ext-MS-Win-NTUser-DialogBox-l1-1-1.dll
-	ext-ms-win-ntuser-dialogbox-l1-1-2.dll
api_name:
-	SetDlgItemText
-	SetDlgItemTextA
-	SetDlgItemTextW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SetDlgItemTextA function


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



The <b>SetDlgItemText</b> function sends a <a href="https://msdn.microsoft.com/1b48c309-6903-4139-bf42-e8526963e681">WM_SETTEXT</a> message to the specified control. 


#### Examples

For an example, see <a href="_win32_Using_List_Boxes">Using List Boxes</a>. 

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/07ebee3c-5aa7-4b0d-b6cb-e642e01e1a88">Dialog Boxes</a>



<a href="https://msdn.microsoft.com/8a0b8275-35e5-4983-9b2d-968023d39aa3">GetDlgItemInt</a>



<a href="https://msdn.microsoft.com/6cfaa693-aafe-4034-abcb-0a8364cccb4b">GetDlgItemText</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8c71aa0e-1287-4a56-bef5-bcdddc9d9332">SetDlgItemInt</a>



<a href="https://msdn.microsoft.com/1b48c309-6903-4139-bf42-e8526963e681">WM_SETTEXT</a>
 

 

