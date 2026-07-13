---
UID: NF:commctrl.Button_SetSplitInfo
title: Button_SetSplitInfo macro (commctrl.h)
description: Sets information for a specified split button control. Use this macro or send the BCM_SETSPLITINFO message explicitly.
helpviewer_keywords: ["Button_SetSplitInfo","Button_SetSplitInfo macro [Windows Controls]","_shell_Button_SetSplitInfo","_shell_Button_SetSplitInfo_cpp","commctrl/Button_SetSplitInfo","controls.Button_SetSplitInfo","controls._shell_Button_SetSplitInfo"]
old-location: controls\Button_SetSplitInfo.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_setsplitinfo.htm
ms.date: 10/21/2024
ms.keywords: Button_SetSplitInfo, Button_SetSplitInfo macro [Windows Controls], _shell_Button_SetSplitInfo, _shell_Button_SetSplitInfo_cpp, commctrl/Button_SetSplitInfo, controls.Button_SetSplitInfo, controls._shell_Button_SetSplitInfo
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
 - Button_SetSplitInfo
 - commctrl/Button_SetSplitInfo
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
 - Button_SetSplitInfo
---

# Button_SetSplitInfo macro

## -syntax

```cpp
BOOL Button_SetSplitInfo(
  [in] HWND             hwnd,
  [in] BUTTON_SPLITINFO *pInfo
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Sets information for a specified split button control. Use this macro or send the <a href="/windows/desktop/Controls/bcm-setsplitinfo">BCM_SETSPLITINFO</a> message explicitly.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the button control.

### -param pInfo [in]

Type: <b><a href="/windows/desktop/api/commctrl/ns-commctrl-button_splitinfo">BUTTON_SPLITINFO</a>*</b>

A pointer to a <a href="/windows/desktop/api/commctrl/ns-commctrl-button_splitinfo">BUTTON_SPLITINFO</a> structure. The calling application is responsible for allocating the memory for this structure and initializing it. Set the <b>mask</b> member of this structure to determine what information to set for the button specified by <i>hwnd</i>.

## -remarks

Use this macro only with the <a href="/windows/desktop/Controls/button-styles">BS_SPLITBUTTON</a> and <a href="/windows/desktop/Controls/button-styles">BS_DEFSPLITBUTTON</a> button styles.

## -see-also

<a href="/windows/desktop/Controls/button-styles">Button Styles</a>



<a href="/windows/desktop/Controls/button-types-and-styles">Button Types</a>



<b>Conceptual</b>



<b>Reference</b>
