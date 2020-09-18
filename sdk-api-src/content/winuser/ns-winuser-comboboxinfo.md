---
UID: NS:winuser.tagCOMBOBOXINFO
title: COMBOBOXINFO (winuser.h)
description: Contains combo box status information.
helpviewer_keywords: ["*LPCOMBOBOXINFO","*PCOMBOBOXINFO","COMBOBOXINFO","COMBOBOXINFO structure [Windows Controls]","LPCOMBOBOXINFO","LPCOMBOBOXINFO structure pointer [Windows Controls]","PCOMBOBOXINFO","PCOMBOBOXINFO structure pointer [Windows Controls]","STATE_SYSTEM_INVISIBLE","STATE_SYSTEM_PRESSED","_win32_COMBOBOXINFO_str","_win32_COMBOBOXINFO_str_cpp","controls.COMBOBOXINFO","controls._win32_COMBOBOXINFO_str","winuser/COMBOBOXINFO","winuser/LPCOMBOBOXINFO","winuser/PCOMBOBOXINFO"]
old-location: controls\COMBOBOXINFO.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxstructures\comboboxinfo.htm
ms.date: 12/05/2018
ms.keywords: '*LPCOMBOBOXINFO, *PCOMBOBOXINFO, COMBOBOXINFO, COMBOBOXINFO structure [Windows Controls], LPCOMBOBOXINFO, LPCOMBOBOXINFO structure pointer [Windows Controls], PCOMBOBOXINFO, PCOMBOBOXINFO structure pointer [Windows Controls], STATE_SYSTEM_INVISIBLE, STATE_SYSTEM_PRESSED, _win32_COMBOBOXINFO_str, _win32_COMBOBOXINFO_str_cpp, controls.COMBOBOXINFO, controls._win32_COMBOBOXINFO_str, winuser/COMBOBOXINFO, winuser/LPCOMBOBOXINFO, winuser/PCOMBOBOXINFO'
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
req.typenames: COMBOBOXINFO, *PCOMBOBOXINFO, *LPCOMBOBOXINFO
req.redist: Service Pack 6
ms.custom: 19H1
f1_keywords:
 - tagCOMBOBOXINFO
 - winuser/tagCOMBOBOXINFO
 - PCOMBOBOXINFO
 - winuser/PCOMBOBOXINFO
 - COMBOBOXINFO
 - winuser/COMBOBOXINFO
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
 - COMBOBOXINFO
---

# COMBOBOXINFO structure


## -description

Contains combo box status information.

## -struct-fields

### -field cbSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

The size, in bytes, of the structure. The calling application must set this to sizeof(COMBOBOXINFO).

### -field rcItem

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

A <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies the coordinates of the edit box.

### -field rcButton

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

A <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies the coordinates of the button that contains the drop-down arrow.

### -field stateButton

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

The combo box button state. This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The button exists and is not pressed.

</td>
</tr>
<tr>
<td width="40%"><a id="STATE_SYSTEM_INVISIBLE"></a><a id="state_system_invisible"></a><dl>
<dt><b>STATE_SYSTEM_INVISIBLE</b></dt>
</dl>
</td>
<td width="60%">
There is no button.

</td>
</tr>
<tr>
<td width="40%"><a id="STATE_SYSTEM_PRESSED"></a><a id="state_system_pressed"></a><dl>
<dt><b>STATE_SYSTEM_PRESSED</b></dt>
</dl>
</td>
<td width="60%">
The button is pressed.

</td>
</tr>
</table>

### -field hwndCombo

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the combo box.

### -field hwndItem

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the edit box.

### -field hwndList

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the drop-down list.

## -remarks

The following example code retrieves information about the combo box specified by the window handle.


```
COMBOBOXINFO info = { sizeof(COMBOBOXINFO) };
GetComboBoxInfo(hwnd, &info);

```

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-getcomboboxinfo">GetComboBoxInfo</a>