---
UID: NF:winuser.GetDlgItem
title: GetDlgItem function
author: windows-sdk-content
description: Retrieves a handle to a control in the specified dialog box.
old-location: dlgbox\getdlgitem.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\getdlgitem.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: GetDlgItem, GetDlgItem function [Dialog Boxes], _win32_GetDlgItem, _win32_getdlgitem_cpp, dlgbox.getdlgitem, winui._win32_getdlgitem, winuser/GetDlgItem
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
 - GetDlgItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetDlgItem function


## -description


Retrieves a handle to a control in the specified dialog box. 


## -parameters




### -param hDlg [in, optional]

Type: <b>HWND</b>

A handle to the dialog box that contains the control. 


### -param nIDDlgItem [in]

Type: <b>int</b>

The identifier of the control to be retrieved. 


## -returns



Type: <b>HWND</b>

If the function succeeds, the return value is the window handle of the specified control. 

If the function fails, the return value is <b>NULL</b>, indicating an invalid dialog box handle or a nonexistent control. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



You can use the <b>GetDlgItem</b> function with any parent-child window pair, not just with dialog boxes. As long as the <i>hDlg</i> parameter specifies a parent window and the child window has a unique identifier (as specified by the <i>hMenu</i> parameter in the <a href="https://msdn.microsoft.com/5424b87c-22ea-414e-840e-214d9f0dc9ad">CreateWindow</a> or <a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a> function that created the child window), <b>GetDlgItem</b> returns a valid handle to the child window. 


#### Examples

For an example, see <a href="using_dialog_boxes.htm">Initializing a Dialog Box</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/5424b87c-22ea-414e-840e-214d9f0dc9ad">CreateWindow</a>



<a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a>



<a href="https://msdn.microsoft.com/07ebee3c-5aa7-4b0d-b6cb-e642e01e1a88">Dialog Boxes</a>



<a href="https://msdn.microsoft.com/8a0b8275-35e5-4983-9b2d-968023d39aa3">GetDlgItemInt</a>



<a href="https://msdn.microsoft.com/6cfaa693-aafe-4034-abcb-0a8364cccb4b">GetDlgItemText</a>



<b>Reference</b>
 

 

