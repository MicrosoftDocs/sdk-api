---
UID: NF:windowsx.Edit_LineLength
title: Edit_LineLength macro (windowsx.h)
description: Retrieves the length, in characters, of a line in an edit or rich edit control. You can use this macro or send the EM_LINELENGTH message explicitly.
helpviewer_keywords: ["Edit_LineLength","Edit_LineLength macro [Windows Controls]","_win32_Edit_LineLength","_win32_Edit_LineLength_cpp","controls.Edit_LineLength","controls._win32_Edit_LineLength","windowsx/Edit_LineLength"]
old-location: controls\Edit_LineLength.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_linelength.htm
ms.date: 10/21/2024
ms.keywords: Edit_LineLength, Edit_LineLength macro [Windows Controls], _win32_Edit_LineLength, _win32_Edit_LineLength_cpp, controls.Edit_LineLength, controls._win32_Edit_LineLength, windowsx/Edit_LineLength
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
 - Edit_LineLength
 - windowsx/Edit_LineLength
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
 - Edit_LineLength
---

# Edit_LineLength macro

## -syntax

```cpp
int Edit_LineLength(
   HWND hwndCtl,
   int  line
);
```

## -returns

Type: **int**

The length of the line.


## -description

Retrieves the length, in characters, of a line in an edit or rich edit control. You can use this macro or send the <a href="/windows/desktop/Controls/em-linelength">EM_LINELENGTH</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param line

Type: <b>int</b>

The zero-based index of the line.

## -remarks

For more information, see <a href="/windows/desktop/Controls/em-linelength">EM_LINELENGTH</a>.
