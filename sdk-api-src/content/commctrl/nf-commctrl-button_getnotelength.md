---
UID: NF:commctrl.Button_GetNoteLength
title: Button_GetNoteLength macro (commctrl.h)
description: Gets the length of the note text that may be displayed in the description for a command link. Use this macro or send the BCM_GETNOTELENGTH message explicitly.
helpviewer_keywords: ["Button_GetNoteLength","Button_GetNoteLength macro [Windows Controls]","_shell_Button_GetNoteLength","_shell_Button_GetNoteLength_cpp","commctrl/Button_GetNoteLength","controls.Button_GetNoteLength","controls._shell_Button_GetNoteLength"]
old-location: controls\Button_GetNoteLength.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_getnotelength.htm
ms.date: 10/21/2024
ms.keywords: Button_GetNoteLength, Button_GetNoteLength macro [Windows Controls], _shell_Button_GetNoteLength, _shell_Button_GetNoteLength_cpp, commctrl/Button_GetNoteLength, controls.Button_GetNoteLength, controls._shell_Button_GetNoteLength
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
 - Button_GetNoteLength
 - commctrl/Button_GetNoteLength
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
 - Button_GetNoteLength
---

# Button_GetNoteLength macro

## -syntax

```cpp
LRESULT Button_GetNoteLength(
  [in] HWND hwnd
);
```

## -returns

Type: **[LRESULT](/windows/desktop/winprog/windows-data-types)**

Returns the length of the note text in <b>WCHAR</b>s, not including any terminating <b>NULL</b>, or zero if there is no note text.

## -description

Gets the length of the note text that may be displayed in the description for a command link. Use this macro or send the <a href="/windows/desktop/Controls/bcm-getnotelength">BCM_GETNOTELENGTH</a> message explicitly.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the button control.

## -remarks

Beginning with comctl32 DLL version 6.01, command link buttons may have a note. For information on DLL versions, see <a href="/windows/desktop/Controls/common-control-versions">Common Control Versions</a>.

The <b>Button_GetNoteLength</b> macro works only with the <a href="/windows/desktop/Controls/button-styles">BS_COMMANDLINK</a> and <a href="/windows/desktop/Controls/button-styles">BS_DEFCOMMANDLINK</a> button styles.

## -see-also

<a href="/windows/desktop/Controls/button-styles">Button Styles</a>



<a href="/windows/desktop/Controls/button-types-and-styles">Button Types</a>



<b>Conceptual</b>



<b>Reference</b>
