---
UID: NF:commctrl.Animate_Create
title: Animate_Create macro (commctrl.h)
description: Creates an animation control. Animate_Create calls the CreateWindow function to create the animation control.
helpviewer_keywords: ["Animate_Create","Animate_Create macro [Windows Controls]","_win32_Animate_Create","_win32_Animate_Create_cpp","commctrl/Animate_Create","controls.Animate_Create","controls._win32_Animate_Create"]
old-location: controls\Animate_Create.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\animation\macros\animate_create.htm
ms.date: 10/21/2024
ms.keywords: Animate_Create, Animate_Create macro [Windows Controls], _win32_Animate_Create, _win32_Animate_Create_cpp, commctrl/Animate_Create, controls.Animate_Create, controls._win32_Animate_Create
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
 - Animate_Create
 - commctrl/Animate_Create
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
 - Animate_Create
---

# Animate_Create macro

## -syntax

```cpp
HWND Animate_Create(
   HWND      hwndP,
   UINT      id,
   DWORD     dwStyle,
   HINSTANCE hInstance
);
```

## -returns

Type: **[HWND](/windows/desktop/winprog/windows-data-types)**

Returns the handle to the animation control.


## -description

Creates an animation control. <b>Animate_Create</b> calls the <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa">CreateWindow</a> function to create the animation control.

## -parameters

### -param hwndP

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the parent window.

### -param id

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The child window identifier of the animation control.

### -param dwStyle

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

The window styles. For a list of the animation control style values, see <a href="/windows/desktop/Controls/animation-control-styles">Animation Control Styles</a>.

### -param hInstance

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HINSTANCE</a></b>

A handle to the instance of the module that is creating the animation control.

## -remarks

The <b>Animate_Create</b> macro sets the width and height of the animation control to zero if the <a href="/windows/desktop/Controls/animation-control-styles">ACS_CENTER</a> style is specified. If the <b>ACS_CENTER</b> style is not specified, <b>Animate_Create</b> sets the width and height based on the dimensions of a frame in the AVI clip.
