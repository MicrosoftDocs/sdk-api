---
UID: NF:commctrl.Edit_NoSetFocus
title: Edit_NoSetFocus macro (commctrl.h)
description: Prevents a single-line edit control from receiving keyboard focus. You can use this macro or send the EM_NOSETFOCUS message explicitly.
helpviewer_keywords: ["Edit_NoSetFocus","Edit_NoSetFocus macro [Windows Controls]","_win32_Edit_NoSetFocus","_win32_Edit_NoSetFocus_cpp","commctrl/Edit_NoSetFocus","controls.Edit_NoSetFocus","controls._win32_Edit_NoSetFocus"]
old-location: controls\Edit_NoSetFocus.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_nosetfocus.htm
ms.date: 10/21/2024
ms.keywords: Edit_NoSetFocus, Edit_NoSetFocus macro [Windows Controls], _win32_Edit_NoSetFocus, _win32_Edit_NoSetFocus_cpp, commctrl/Edit_NoSetFocus, controls.Edit_NoSetFocus, controls._win32_Edit_NoSetFocus
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Edit_NoSetFocus
 - commctrl/Edit_NoSetFocus
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
 - Edit_NoSetFocus
---

# Edit_NoSetFocus macro

## -syntax

```cpp
DWORD Edit_NoSetFocus(
   HWND hwndCtl
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

The return value is not used.


## -description

<p class="CCE_Message">[Intended for internal use; not recommended for use in applications. This macro may not be supported in future versions of Windows.]

Prevents a single-line edit control from receiving keyboard focus. You can use this macro or send the <a href="/windows/desktop/Controls/em-nosetfocus">EM_NOSETFOCUS</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the edit control.

## -remarks

The <a href="/windows/desktop/Controls/em-nosetfocus">EM_NOSETFOCUS</a> message is ignored if the edit control is not a single-line edit control. 

After this message is sent, the effect is permanent.

## -see-also

<a href="/windows/desktop/Controls/em-nosetfocus">EM_NOSETFOCUS</a>
