---
UID: NF:winuser.GetDlgCtrlID
title: GetDlgCtrlID function
author: windows-sdk-content
description: Retrieves the identifier of the specified control.
old-location: dlgbox\getdlgctrlid.htm
old-project: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\getdlgctrlid.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: GetDlgCtrlID, GetDlgCtrlID function [Dialog Boxes], _win32_GetDlgCtrlID, _win32_getdlgctrlid_cpp, dlgbox.getdlgctrlid, winui._win32_getdlgctrlid, winuser/GetDlgCtrlID
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
tech.root: 
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
-	GetDlgCtrlID
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetDlgCtrlID function


## -description


Retrieves the identifier of the specified control. 


## -parameters




### -param hWnd

TBD




#### - hwndCtl [in]

Type: <b>HWND</b>

A handle to the control. 


## -returns



Type: <b>int</b>

If the function succeeds, the return value is the identifier of the control.

If the function fails, the return value is zero. An invalid value for the <i>hwndCtl</i> parameter, for example, will cause the function to fail. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<b>GetDlgCtrlID</b> accepts child window handles as well as handles of controls in dialog boxes. An application sets the identifier for a child window when it creates the window by assigning the identifier value to the <i>hmenu</i> parameter when calling the <a href="https://msdn.microsoft.com/5424b87c-22ea-414e-840e-214d9f0dc9ad">CreateWindow</a> or <a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a> function. 

Although <b>GetDlgCtrlID</b> may return a value if <i>hwndCtl</i> is a handle to a top-level window, top-level windows cannot have identifiers and such a return value is never valid. 


#### Examples


			
			For an example, see <a href="using_dialog_boxes.htm">Initializing a Dialog Box</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/5424b87c-22ea-414e-840e-214d9f0dc9ad">CreateWindow</a>



<a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a>



<a href="https://msdn.microsoft.com/07ebee3c-5aa7-4b0d-b6cb-e642e01e1a88">Dialog Boxes</a>



<a href="https://msdn.microsoft.com/c119d716-b07f-4644-9d51-da94fab3e516">GetDlgItem</a>



<b>Reference</b>
 

 

