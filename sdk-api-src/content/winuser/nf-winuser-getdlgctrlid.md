---
UID: NF:winuser.GetDlgCtrlID
title: GetDlgCtrlID function
author: windows-sdk-content
description: Retrieves the identifier of the specified control.
old-location: dlgbox\getdlgctrlid.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\getdlgctrlid.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: GetDlgCtrlID, GetDlgCtrlID function [Dialog Boxes], _win32_GetDlgCtrlID, _win32_getdlgctrlid_cpp, dlgbox.getdlgctrlid, winui._win32_getdlgctrlid, winuser/GetDlgCtrlID
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
req.unicode-ansi: 
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
 - GetDlgCtrlID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetDlgCtrlID function


## -description


Retrieves the identifier of the specified control. 


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the control. 


## -returns



Type: <b>int</b>

If the function succeeds, the return value is the identifier of the control.

If the function fails, the return value is zero. An invalid value for the <i>hwndCtl</i> parameter, for example, will cause the function to fail. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<b>GetDlgCtrlID</b> accepts child window handles as well as handles of controls in dialog boxes. An application sets the identifier for a child window when it creates the window by assigning the identifier value to the <i>hmenu</i> parameter when calling the <a href="https://msdn.microsoft.com/en-us/library/ms632679(v=VS.85).aspx">CreateWindow</a> or <a href="https://msdn.microsoft.com/en-us/library/ms632680(v=VS.85).aspx">CreateWindowEx</a> function. 

Although <b>GetDlgCtrlID</b> may return a value if <i>hwndCtl</i> is a handle to a top-level window, top-level windows cannot have identifiers and such a return value is never valid. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms644996(v=VS.85).aspx">Initializing a Dialog Box</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632679(v=VS.85).aspx">CreateWindow</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632680(v=VS.85).aspx">CreateWindowEx</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632588(v=VS.85).aspx">Dialog Boxes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645481(v=VS.85).aspx">GetDlgItem</a>



<b>Reference</b>
 

 

