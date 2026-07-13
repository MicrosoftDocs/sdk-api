---
UID: NF:commctrl.Edit_ShowBalloonTip
title: Edit_ShowBalloonTip macro (commctrl.h)
description: Displays a balloon tip associated with an edit control. You can use this macro or send the EM_SHOWBALLOONTIP message explicitly.
helpviewer_keywords: ["Edit_ShowBalloonTip","Edit_ShowBalloonTip macro [Windows Controls]","_win32_Edit_ShowBalloonTip","_win32_Edit_ShowBalloonTip_cpp","commctrl/Edit_ShowBalloonTip","controls.Edit_ShowBalloonTip","controls._win32_Edit_ShowBalloonTip"]
old-location: controls\Edit_ShowBalloonTip.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_showballoontip.htm
ms.date: 10/21/2024
ms.keywords: Edit_ShowBalloonTip, Edit_ShowBalloonTip macro [Windows Controls], _win32_Edit_ShowBalloonTip, _win32_Edit_ShowBalloonTip_cpp, commctrl/Edit_ShowBalloonTip, controls.Edit_ShowBalloonTip, controls._win32_Edit_ShowBalloonTip
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
 - Edit_ShowBalloonTip
 - commctrl/Edit_ShowBalloonTip
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
 - Edit_ShowBalloonTip
---

# Edit_ShowBalloonTip macro

## -syntax

```cpp
BOOL Edit_ShowBalloonTip(
   HWND            hwnd,
   PEDITBALLOONTIP peditballoontip
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

If the macro succeeds, it returns <b>TRUE</b>. Otherwise it returns <b>FALSE</b>.


## -description

Displays a balloon tip associated with an edit control. You can use this macro or send the <a href="/windows/desktop/Controls/em-showballoontip">EM_SHOWBALLOONTIP</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the edit control.

### -param peditballoontip

Type: <b>PEDITBALLOONTIP</b>

A pointer to an <a href="/windows/desktop/api/commctrl/ns-commctrl-editballoontip">EDITBALLOONTIP</a> structure that contains information about the balloon tip to display.

## -remarks

<div class="alert"><b>Note</b>  To use this macro, you must provide a manifest specifying Comctl32.dll version 6.0. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.</div>
<div> </div>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/commctrl/ns-commctrl-editballoontip">EDITBALLOONTIP</a>



<a href="/windows/desktop/Controls/em-showballoontip">EM_SHOWBALLOONTIP</a>



<a href="/windows/desktop/Controls/edit-controls">Edit Controls</a>



<b>Reference</b>
