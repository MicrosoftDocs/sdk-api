---
UID: NS:winuser.tagCOMPAREITEMSTRUCT
title: COMPAREITEMSTRUCT (winuser.h)
description: Supplies the identifiers and application-supplied data for two items in a sorted, owner-drawn list box or combo box.
helpviewer_keywords: ["*LPCOMPAREITEMSTRUCT","*PCOMPAREITEMSTRUCT","COMPAREITEMSTRUCT","COMPAREITEMSTRUCT structure [Windows Controls]","_win32_COMPAREITEMSTRUCT_str","_win32_COMPAREITEMSTRUCT_str_cpp","controls.COMPAREITEMSTRUCT","controls._win32_COMPAREITEMSTRUCT_str","winuser/COMPAREITEMSTRUCT"]
old-location: controls\COMPAREITEMSTRUCT.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxstructures\compareitemstruct.htm
ms.date: 12/05/2018
ms.keywords: '*LPCOMPAREITEMSTRUCT, *PCOMPAREITEMSTRUCT, COMPAREITEMSTRUCT, COMPAREITEMSTRUCT structure [Windows Controls], _win32_COMPAREITEMSTRUCT_str, _win32_COMPAREITEMSTRUCT_str_cpp, controls.COMPAREITEMSTRUCT, controls._win32_COMPAREITEMSTRUCT_str, winuser/COMPAREITEMSTRUCT'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: COMPAREITEMSTRUCT, *PCOMPAREITEMSTRUCT, *LPCOMPAREITEMSTRUCT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCOMPAREITEMSTRUCT
 - winuser/tagCOMPAREITEMSTRUCT
 - PCOMPAREITEMSTRUCT
 - winuser/PCOMPAREITEMSTRUCT
 - COMPAREITEMSTRUCT
 - winuser/COMPAREITEMSTRUCT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - COMPAREITEMSTRUCT
---

# COMPAREITEMSTRUCT structure


## -description

Supplies the identifiers and application-supplied data for two items in a sorted, owner-drawn list box or combo box.

Whenever an application adds a new item to an owner-drawn list box or combo box created with the <a href="/windows/desktop/Controls/combo-box-styles">CBS_SORT</a> or <a href="/windows/desktop/Controls/list-box-styles">LBS_SORT</a> style, the system sends the owner a <a href="/windows/desktop/Controls/wm-compareitem">WM_COMPAREITEM</a> message. The <i>lParam</i> parameter of the message contains a long pointer to a <b>COMPAREITEMSTRUCT</b> structure. Upon receiving the message, the owner compares the two items and returns a value indicating which item sorts before the other.

## -struct-fields

### -field CtlType

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

An ODT_LISTBOX (owner-drawn list box) or ODT_COMBOBOX (an owner-drawn combo box).

### -field CtlID

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The identifier of the list box or combo box.

### -field hwndItem

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -field itemID1

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the first item in the list box or combo box being compared. This member will be –1 if the item has not been inserted or when searching for a potential item in the list box or combo box.

### -field itemData1

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">ULONG_PTR</a></b>

Application-supplied data for the first item being compared. (This value was passed as the <i>lParam</i> parameter of the message that added the item to the list box or combo box.)

### -field itemID2

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the second item in the list box or combo box being compared.

### -field itemData2

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">ULONG_PTR</a></b>

Application-supplied data for the second item being compared. This value was passed as the 
					<i>lParam</i> parameter of the message that added the item to the list box or combo box. This member will be 
					–1 if the item has not been inserted or when searching for a potential item in the list box or combo box.

### -field dwLocaleId

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

The locale identifier. To create a locale identifier, use the <a href="/windows/desktop/api/winnt/nf-winnt-makelcid">MAKELCID</a> macro.

## -see-also

<a href="/windows/desktop/Controls/combo-boxes">Combo Boxes</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winnt/nf-winnt-makelcid">MAKELCID</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/Controls/wm-compareitem">WM_COMPAREITEM</a>