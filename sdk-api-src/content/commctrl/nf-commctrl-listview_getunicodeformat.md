---
UID: NF:commctrl.ListView_GetUnicodeFormat
title: ListView_GetUnicodeFormat macro (commctrl.h)
description: Gets the Unicode character format flag for the control. You can use this macro or send the LVM_GETUNICODEFORMAT message explicitly.
helpviewer_keywords: ["ListView_GetUnicodeFormat","ListView_GetUnicodeFormat macro [Windows Controls]","_win32_ListView_GetUnicodeFormat","_win32_ListView_GetUnicodeFormat_cpp","commctrl/ListView_GetUnicodeFormat","controls.ListView_GetUnicodeFormat","controls._win32_ListView_GetUnicodeFormat"]
old-location: controls\ListView_GetUnicodeFormat.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getunicodeformat.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetUnicodeFormat, ListView_GetUnicodeFormat macro [Windows Controls], _win32_ListView_GetUnicodeFormat, _win32_ListView_GetUnicodeFormat_cpp, commctrl/ListView_GetUnicodeFormat, controls.ListView_GetUnicodeFormat, controls._win32_ListView_GetUnicodeFormat
req.header: commctrl.h
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
 - ListView_GetUnicodeFormat
 - commctrl/ListView_GetUnicodeFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - ListView_GetUnicodeFormat
---

# ListView_GetUnicodeFormat macro

## -syntax

```cpp
BOOL ListView_GetUnicodeFormat(
   HWND hwnd
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns the Unicode format flag for the control. If this value is nonzero, the control is using Unicode characters. If this value is zero, the control is using ANSI characters.


## -description

Gets the Unicode character format flag for the control. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-getunicodeformat">LVM_GETUNICODEFORMAT</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-listview_setunicodeformat">ListView_SetUnicodeFormat</a>
