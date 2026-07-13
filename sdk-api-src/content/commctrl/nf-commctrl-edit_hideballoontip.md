---
UID: NF:commctrl.Edit_HideBalloonTip
title: Edit_HideBalloonTip macro (commctrl.h)
description: Hides any balloon tip associated with an edit control. You can use this macro or send the EM_HIDEBALLOONTIP message explicitly.
helpviewer_keywords: ["Edit_HideBalloonTip","Edit_HideBalloonTip macro [Windows Controls]","_win32_Edit_HideBalloonTip","_win32_Edit_HideBalloonTip_cpp","commctrl/Edit_HideBalloonTip","controls.Edit_HideBalloonTip","controls._win32_Edit_HideBalloonTip"]
old-location: controls\Edit_HideBalloonTip.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_hideballoontip.htm
ms.date: 10/21/2024
ms.keywords: Edit_HideBalloonTip, Edit_HideBalloonTip macro [Windows Controls], _win32_Edit_HideBalloonTip, _win32_Edit_HideBalloonTip_cpp, commctrl/Edit_HideBalloonTip, controls.Edit_HideBalloonTip, controls._win32_Edit_HideBalloonTip
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
 - Edit_HideBalloonTip
 - commctrl/Edit_HideBalloonTip
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
 - Edit_HideBalloonTip
---

# Edit_HideBalloonTip macro

## -syntax

```cpp
BOOL Edit_HideBalloonTip(
   HWND hwnd
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

If the macro succeeds, it returns <b>TRUE</b>. Otherwise it returns <b>FALSE</b>.


## -description

Hides any balloon tip associated with an edit control. You can use this macro or send the <a href="/windows/desktop/Controls/em-hideballoontip">EM_HIDEBALLOONTIP</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the edit control.

## -remarks

<div class="alert"><b>Note</b>  To use this macro, you must provide a manifest specifying Comctl32.dll version 6.0. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.</div>
<div> </div>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/Controls/em-hideballoontip">EM_HIDEBALLOONTIP</a>



<a href="/windows/desktop/Controls/edit-controls">Edit Controls</a>



<b>Reference</b>
