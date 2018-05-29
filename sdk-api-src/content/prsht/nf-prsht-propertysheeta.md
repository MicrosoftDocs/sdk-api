---
UID: NF:prsht.PropertySheetA
title: PropertySheetA function
author: windows-sdk-content
description: Creates a property sheet and adds the pages defined in the specified property sheet header structure.
old-location: controls\PropertySheet.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\propsheet\functions\propertysheet.htm
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: PropertySheet, PropertySheet function [Windows Controls], PropertySheetA, PropertySheetW, _win32_PropertySheet, _win32_PropertySheet_cpp, controls.PropertySheet, controls._win32_PropertySheet, prsht/PropertySheet, prsht/PropertySheetA, prsht/PropertySheetW
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Comctl32.dll
api_name:
-	PropertySheet
-	PropertySheetA
-	PropertySheetW
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PropertySheetA function


## -description


Creates a property sheet and adds the pages defined in the specified property sheet header structure.


## -parameters




### -param Arg1

TBD




#### - lppsph

Type: <b>LPCPROPSHEETHEADER</b>

Pointer to a <a href="https://msdn.microsoft.com/ed4eb370-593f-4893-9de4-1ea9a725b131">PROPSHEETHEADER</a> structure that defines the frame and pages of a property sheet.


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
A page sent the <a href="https://msdn.microsoft.com/461fce3c-183a-4b9b-8eab-ed2838d9f866">PSM_REBOOTSYSTEM</a> message to the property sheet. The computer must be restarted for the user's changes to take effect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ID_PSRESTARTWINDOWS</b></dt>
</dl>
</td>
<td width="60%">
A page sent the <a href="https://msdn.microsoft.com/5bf634ee-7408-45df-adb6-c5b947f6c47b">PSM_RESTARTWINDOWS</a> message to the property sheet. Windows must be restarted for the user's changes to take effect.

</td>
</tr>
</table>
 




## -remarks



To retrieve extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If you attempt to add more than 99 pages to a property sheet, this function will fail, but with no indication of the cause of the error: <b>PropertySheet</b> returns a value of -1, but <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns 0.

<div class="alert"><b>Note</b>  The following remarks refer only to wizards that do not use the Aero wizard style (<a href="https://msdn.microsoft.com/ed4eb370-593f-4893-9de4-1ea9a725b131">PSH_AEROWIZARD</a>) or non-wizard property sheets.</div>
<div> </div>
By default, the <b>PropertySheet</b> function creates a modal dialog box. If the <b>dwFlags</b> member of the <a href="https://msdn.microsoft.com/ed4eb370-593f-4893-9de4-1ea9a725b131">PROPSHEETHEADER</a> structure specifies the PSH_MODELESS flag, <b>PropertySheet</b> creates a modeless dialog box and returns immediately after it is created. In this case, the <b>PropertySheet</b> return value is the window handle to the modeless dialog box.

For a modeless property sheet, your message loop should use <a href="https://msdn.microsoft.com/7629c3f8-0b10-4585-8a95-9309c75b3ebb">PSM_ISDIALOGMESSAGE</a> to pass messages to the property sheet dialog box. Your message loop should use <a href="https://msdn.microsoft.com/1f2d0af9-5853-48e7-b827-483be032b6ca">PSM_GETCURRENTPAGEHWND</a> to determine when to destroy the dialog box. When the user clicks the <b>OK</b> or <b>Cancel</b> button, <b>PSM_GETCURRENTPAGEHWND</b> returns <b>NULL</b>. You can then use the <a href="https://msdn.microsoft.com/054fa847-7d6e-4c73-bf8c-b75203713b3e">DestroyWindow</a> function to destroy the dialog box.


<a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Version 5.80.</a> The <b>PropertySheet</b> return value carries different information for modal and modeless property sheets. In some cases, modeless property sheets might need the information they would have received from <b>PropertySheet</b> if they had been modal. In particular, they may need to know whether ID_PSREBOOTSYSTEM or ID_PSRESTARTWINDOWS would have been returned. A modeless property sheet can retrieve the value that a modal property sheet would have received from <b>PropertySheet</b> by waiting until <a href="https://msdn.microsoft.com/1f2d0af9-5853-48e7-b827-483be032b6ca">PSM_GETCURRENTPAGEHWND</a> returns <b>NULL</b> and then sending a <a href="https://msdn.microsoft.com/e0f609ea-5d7e-4c17-ade1-3c1051c5a5bf">PSM_GETRESULT</a> message.



