---
UID: NF:winuser.GetComboBoxInfo
title: GetComboBoxInfo function (winuser.h)
description: Retrieves information about the specified combo box.
helpviewer_keywords: ["GetComboBoxInfo","GetComboBoxInfo function [Windows Controls]","_win32_GetComboBoxInfo","_win32_GetComboBoxInfo_cpp","controls.GetComboBoxInfo","controls._win32_GetComboBoxInfo","winuser/GetComboBoxInfo"]
old-location: controls\GetComboBoxInfo.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxfunctions\getcomboboxinfo.htm
ms.date: 12/05/2018
ms.keywords: GetComboBoxInfo, GetComboBoxInfo function [Windows Controls], _win32_GetComboBoxInfo, _win32_GetComboBoxInfo_cpp, controls.GetComboBoxInfo, controls._win32_GetComboBoxInfo, winuser/GetComboBoxInfo
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Service Pack 6
ms.custom: 19H1
f1_keywords:
 - GetComboBoxInfo
 - winuser/GetComboBoxInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - ext-ms-win-ntuser-dialogbox-l1-1-2.dll
api_name:
 - GetComboBoxInfo
req.apiset: ext-ms-win-ntuser-dialogbox-l1-1-2 (introduced in Windows 10, version 10.0.10240)
---

# GetComboBoxInfo function


## -description

Retrieves information about the specified combo box.

## -parameters

### -param hwndCombo [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the combo box.

### -param pcbi [out]

Type: <b>PCOMBOBOXINFO</b>

A pointer to a <a href="/windows/desktop/api/winuser/ns-winuser-comboboxinfo">COMBOBOXINFO</a> structure that receives the information. You must set <b>COMBOBOXINFO.cbSize</b> before calling this function.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <a href="/windows/desktop/Controls/cb-getcomboboxinfo">CB_GETCOMBOBOXINFO</a> message is equivalent to this function.


#### Examples

The following example code retrieves information about the combo box specified by the window handle.


```cpp
COMBOBOXINFO info = { sizeof(COMBOBOXINFO) };
GetComboBoxInfo(hwnd, &info);

```

## -see-also

<a href="/windows/desktop/Controls/cb-getcomboboxinfo">CB_GETCOMBOBOXINFO</a>



<a href="/windows/desktop/api/winuser/ns-winuser-comboboxinfo">COMBOBOXINFO</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getlistboxinfo">GetListBoxInfo</a>



<b>Reference</b>
