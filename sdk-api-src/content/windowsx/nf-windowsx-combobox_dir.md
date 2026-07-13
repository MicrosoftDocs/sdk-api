---
UID: NF:windowsx.ComboBox_Dir
title: ComboBox_Dir macro (windowsx.h)
description: Adds names to the list displayed by a combo box.
helpviewer_keywords: ["ComboBox_Dir","ComboBox_Dir macro [Windows Controls]","_win32_ComboBox_Dir","_win32_ComboBox_Dir_cpp","controls.ComboBox_Dir","controls._win32_ComboBox_Dir","windowsx/ComboBox_Dir"]
old-location: controls\ComboBox_Dir.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_dir.htm
ms.date: 10/21/2024
ms.keywords: ComboBox_Dir, ComboBox_Dir macro [Windows Controls], _win32_ComboBox_Dir, _win32_ComboBox_Dir_cpp, controls.ComboBox_Dir, controls._win32_ComboBox_Dir, windowsx/ComboBox_Dir
req.header: windowsx.h
req.include-header: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ComboBox_Dir
 - windowsx/ComboBox_Dir
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windowsx.h
api_name:
 - ComboBox_Dir
---

# ComboBox_Dir macro

## -syntax

```cpp
int ComboBox_Dir(
   HWND    hwndCtl,
   UINT    attrs,
   LPCTSTR lpszFileSpec
);
```

## -returns

Type: **int**

If the message succeeds, the return value is the zero-based index of the last name added to the list. If an error occurs, the return value is CB_ERR. If there is insufficient space to store the new strings, the return value is CB_ERRSPACE.


## -description

Adds names to the list displayed by a combo box. The macro adds the names of directories and files that match a specified string and set of file attributes. It can also add mapped drive letters to the list in a combo box. You can use this macro or send the <a href="/windows/desktop/Controls/cb-dir">CB_DIR</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param attrs

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The attributes of the files or directories to be added to the list in a combo box. For more information, see <a href="/windows/desktop/Controls/cb-dir">CB_DIR</a>.

### -param lpszFileSpec

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

A pointer to the null-terminated string that specifies an absolute path, relative path, or filename. An absolute path can begin with a drive letter (for example, d:\) or a UNC name (for example, \\ machinename\ sharename).

## -remarks

For more information, see <a href="/windows/desktop/Controls/cb-dir">CB_DIR</a>.
