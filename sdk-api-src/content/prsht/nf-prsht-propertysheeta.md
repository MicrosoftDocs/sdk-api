---
UID: NF:prsht.PropertySheetA
title: PropertySheetA function (prsht.h)
description: Creates a property sheet and adds the pages defined in the specified property sheet header structure. (ANSI)
helpviewer_keywords: ["PropertySheetA", "prsht/PropertySheetA"]
old-location: controls\PropertySheet.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\functions\propertysheet.htm
ms.date: 12/05/2018
ms.keywords: PropertySheet, PropertySheet function [Windows Controls], PropertySheetA, PropertySheetW, _win32_PropertySheet, _win32_PropertySheet_cpp, controls.PropertySheet, controls._win32_PropertySheet, prsht/PropertySheet, prsht/PropertySheetA, prsht/PropertySheetW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PropertySheetA
 - prsht/PropertySheetA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
 - ext-ms-win-shell-comctl32-window-l1-1-0.dll
api_name:
 - PropertySheet
 - PropertySheetA
 - PropertySheetW
req.apiset: ext-ms-win-shell-comctl32-window-l1-1-0 (introduced in Windows 10, version 10.0.14393)
---

# PropertySheetA function


## -description

Creates a property sheet and adds the pages defined in the specified property sheet header structure.

## -parameters

### -param unnamedParam1

Type: <b>LPCPROPSHEETHEADER</b>

Pointer to a <a href="/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PROPSHEETHEADER</a> structure that defines the frame and pages of a property sheet.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT_PTR</a></b>

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
A page sent the <a href="/windows/desktop/Controls/psm-rebootsystem">PSM_REBOOTSYSTEM</a> message to the property sheet. The computer must be restarted for the user's changes to take effect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ID_PSRESTARTWINDOWS</b></dt>
</dl>
</td>
<td width="60%">
A page sent the <a href="/windows/desktop/Controls/psm-restartwindows">PSM_RESTARTWINDOWS</a> message to the property sheet. Windows must be restarted for the user's changes to take effect.

</td>
</tr>
</table>

## -remarks

To retrieve extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If you attempt to add more than 99 pages to a property sheet, this function will fail, but with no indication of the cause of the error: <b>PropertySheet</b> returns a value of -1, but <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns 0.

<div class="alert"><b>Note</b>  The following remarks refer only to wizards that do not use the Aero wizard style (<a href="/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PSH_AEROWIZARD</a>) or non-wizard property sheets.</div>
<div> </div>
By default, the <b>PropertySheet</b> function creates a modal dialog box. If the <b>dwFlags</b> member of the <a href="/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PROPSHEETHEADER</a> structure specifies the PSH_MODELESS flag, <b>PropertySheet</b> creates a modeless dialog box and returns immediately after it is created. In this case, the <b>PropertySheet</b> return value is the window handle to the modeless dialog box.

For a modeless property sheet, your message loop should use <a href="/windows/desktop/Controls/psm-isdialogmessage">PSM_ISDIALOGMESSAGE</a> to pass messages to the property sheet dialog box. Your message loop should use <a href="/windows/desktop/Controls/psm-getcurrentpagehwnd">PSM_GETCURRENTPAGEHWND</a> to determine when to destroy the dialog box. When the user clicks the <b>OK</b> or <b>Cancel</b> button, <b>PSM_GETCURRENTPAGEHWND</b> returns <b>NULL</b>. You can then use the <a href="/windows/desktop/api/winuser/nf-winuser-destroywindow">DestroyWindow</a> function to destroy the dialog box.


<a href="/windows/desktop/Controls/common-control-versions">Version 5.80.</a> The <b>PropertySheet</b> return value carries different information for modal and modeless property sheets. In some cases, modeless property sheets might need the information they would have received from <b>PropertySheet</b> if they had been modal. In particular, they may need to know whether ID_PSREBOOTSYSTEM or ID_PSRESTARTWINDOWS would have been returned. A modeless property sheet can retrieve the value that a modal property sheet would have received from <b>PropertySheet</b> by waiting until <a href="/windows/desktop/Controls/psm-getcurrentpagehwnd">PSM_GETCURRENTPAGEHWND</a> returns <b>NULL</b> and then sending a <a href="/windows/desktop/Controls/psm-getresult">PSM_GETRESULT</a> message.




> [!NOTE]
> The prsht.h header defines PropertySheet as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
