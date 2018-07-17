---
UID: NF:winuser.CheckRadioButton
title: CheckRadioButton function
author: windows-sdk-content
description: Adds a check mark to (checks) a specified radio button in a group and removes a check mark from (clears) all other radio buttons in the group.
old-location: controls\CheckRadioButton.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonfunctions\checkradiobutton.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: CheckRadioButton, CheckRadioButton function [Windows Controls], _win32_CheckRadioButton, _win32_CheckRadioButton_cpp, controls.CheckRadioButton, controls._win32_CheckRadioButton, winuser/CheckRadioButton
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - ext-ms-win-ntuser-dialogbox-l1-1-2.dll
api_name:
 - CheckRadioButton
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# CheckRadioButton function


## -description


Adds a check mark to (checks) a specified radio button in a group and removes a check mark from (clears) all other radio buttons in the group. 


## -parameters




### -param hDlg [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the dialog box that contains the radio button. 


### -param nIDFirstButton [in]

Type: <b>int</b>

The identifier of the first radio button in the group. 


### -param nIDLastButton [in]

Type: <b>int</b>

The identifier of the last radio button in the group. 


### -param nIDCheckButton [in]

Type: <b>int</b>

The identifier of the radio button to select. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The <b>CheckRadioButton</b> function sends a <a href="https://msdn.microsoft.com/8294e6c4-caac-4c60-85ff-38698a1d2ae4">BM_SETCHECK</a> message to each of the radio buttons in the indicated group.

The <i>nIDFirstButton</i> and <i>nIDLastButton</i> parameters specify a range of button identifiers (normally the resource IDs of the buttons).  The position of buttons in the tab order is irrelevant; if a button forms part of a group, but has an ID outside the specified range, it is not affected by this call.




## -see-also




<a href="https://msdn.microsoft.com/bda42841-cc26-44c7-9295-3b3bc818d269">CheckDlgButton</a>



<a href="https://msdn.microsoft.com/859ff84e-a6d8-466b-9b85-f844a47febdf">IsDlgButtonChecked</a>



<b>Reference</b>
 

 

