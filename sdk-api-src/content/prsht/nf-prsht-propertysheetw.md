---
UID: NF:prsht.PropertySheetW
title: PropertySheetW function
author: windows-sdk-content
description: Creates a property sheet and adds the pages defined in the specified property sheet header structure.
old-location: controls\PropertySheet.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\functions\propertysheet.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PropertySheet, PropertySheet function [Windows Controls], PropertySheetA, PropertySheetW, _win32_PropertySheet, _win32_PropertySheet_cpp, controls.PropertySheet, controls._win32_PropertySheet, prsht/PropertySheet, prsht/PropertySheetA, prsht/PropertySheetW
ms.topic: function
req.header: prsht.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PropertySheetW (Unicode) and PropertySheetA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - PropertySheet
 - PropertySheetA
 - PropertySheetW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PropertySheetW function


## -description


Creates a property sheet and adds the pages defined in the specified property sheet header structure.


## -parameters




### -param Arg1

Type: <b>LPCPROPSHEETHEADER</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb774546(v=VS.85).aspx">PROPSHEETHEADER</a> structure that defines the frame and pages of a property sheet.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT_PTR</a></b>

For modal property sheets, the return value is as follows:
                
                

<table class="clsStd">
<tr>
<td>&gt;=1</td>
<td>Changes were saved by the user.</td>
</tr>
<tr>
<td>0</td>
<td>No changes were saved by the user.</td>
</tr>
<tr>
<td>-1</td>
<td>An error occurred.</td>
</tr>
</table>
 

For modeless property sheets, the return value is  the property sheet's window handle.

The following return values have a special meaning.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ID_PSREBOOTSYSTEM</b></dt>
</dl>
</td>
<td width="60%">
A page sent the <a href="https://msdn.microsoft.com/en-us/library/Bb774601(v=VS.85).aspx">PSM_REBOOTSYSTEM</a> message to the property sheet. The computer must be restarted for the user's changes to take effect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ID_PSRESTARTWINDOWS</b></dt>
</dl>
</td>
<td width="60%">
A page sent the <a href="https://msdn.microsoft.com/en-us/library/Bb774607(v=VS.85).aspx">PSM_RESTARTWINDOWS</a> message to the property sheet. Windows must be restarted for the user's changes to take effect.

</td>
</tr>
</table>
 




## -remarks



To retrieve extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If you attempt to add more than 99 pages to a property sheet, this function will fail, but with no indication of the cause of the error: <b>PropertySheet</b> returns a value of -1, but <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns 0.

<div class="alert"><b>Note</b>  The following remarks refer only to wizards that do not use the Aero wizard style (<a href="https://msdn.microsoft.com/en-us/library/Bb774546(v=VS.85).aspx">PSH_AEROWIZARD</a>) or non-wizard property sheets.</div>
<div> </div>
By default, the <b>PropertySheet</b> function creates a modal dialog box. If the <b>dwFlags</b> member of the <a href="https://msdn.microsoft.com/en-us/library/Bb774546(v=VS.85).aspx">PROPSHEETHEADER</a> structure specifies the PSH_MODELESS flag, <b>PropertySheet</b> creates a modeless dialog box and returns immediately after it is created. In this case, the <b>PropertySheet</b> return value is the window handle to the modeless dialog box.

For a modeless property sheet, your message loop should use <a href="https://msdn.microsoft.com/en-us/library/Bb774593(v=VS.85).aspx">PSM_ISDIALOGMESSAGE</a> to pass messages to the property sheet dialog box. Your message loop should use <a href="https://msdn.microsoft.com/en-us/library/Bb774578(v=VS.85).aspx">PSM_GETCURRENTPAGEHWND</a> to determine when to destroy the dialog box. When the user clicks the <b>OK</b> or <b>Cancel</b> button, <b>PSM_GETCURRENTPAGEHWND</b> returns <b>NULL</b>. You can then use the <a href="https://msdn.microsoft.com/en-us/library/ms632682(v=VS.85).aspx">DestroyWindow</a> function to destroy the dialog box.


<a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Version 5.80.</a> The <b>PropertySheet</b> return value carries different information for modal and modeless property sheets. In some cases, modeless property sheets might need the information they would have received from <b>PropertySheet</b> if they had been modal. In particular, they may need to know whether ID_PSREBOOTSYSTEM or ID_PSRESTARTWINDOWS would have been returned. A modeless property sheet can retrieve the value that a modal property sheet would have received from <b>PropertySheet</b> by waiting until <a href="https://msdn.microsoft.com/en-us/library/Bb774578(v=VS.85).aspx">PSM_GETCURRENTPAGEHWND</a> returns <b>NULL</b> and then sending a <a href="https://msdn.microsoft.com/en-us/library/Bb774579(v=VS.85).aspx">PSM_GETRESULT</a> message.



