---
UID: NF:commctrl.Animate_OpenEx
title: Animate_OpenEx macro (commctrl.h)
description: Opens an AVI clip from a resource in a specified module and displays its first frame in an animation control. You can use this macro or send the ACM_OPEN message explicitly.
helpviewer_keywords: ["Animate_OpenEx","Animate_OpenEx macro [Windows Controls]","_win32_Animate_OpenEx","_win32_Animate_OpenEx_cpp","commctrl/Animate_OpenEx","controls.Animate_OpenEx","controls._win32_Animate_OpenEx"]
old-location: controls\Animate_OpenEx.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\animation\macros\animate_openex.htm
ms.date: 10/21/2024
ms.keywords: Animate_OpenEx, Animate_OpenEx macro [Windows Controls], _win32_Animate_OpenEx, _win32_Animate_OpenEx_cpp, commctrl/Animate_OpenEx, controls.Animate_OpenEx, controls._win32_Animate_OpenEx
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
 - Animate_OpenEx
 - commctrl/Animate_OpenEx
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
 - Animate_OpenEx
---

# Animate_OpenEx macro

## -syntax

```cpp
BOOL Animate_OpenEx(
   HWND      hwnd,
   HINSTANCE hInst,
   LPTSTR    szName
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns nonzero if successful, or zero otherwise.


## -description

Opens an AVI clip from a resource in a specified module and displays its first frame in an animation control. You can use this macro or send the <a href="/windows/desktop/Controls/acm-open">ACM_OPEN</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the animation control.

### -param hInst

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HINSTANCE</a></b>

An instance handle to the module from which the resource should be loaded. If this value is <b>NULL</b>, the resource is loaded from the module that created the animation control.

### -param szName

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

A pointer to a buffer that contains the path of the AVI file or the name of an AVI resource. Alternatively, this parameter can consist of the AVI resource identifier in the <a href="/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)">LOWORD</a> and zero in the <a href="/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)">HIWORD</a>. To create this value, use the <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro. The control loads the AVI resource from the module specified by <i>hInst</i>. The AVI file or resource specified by <i>szName</i> must not contain audio.



If this parameter is <b>NULL</b>, the system closes the AVI file that was previously opened for the specified animation control, if any.

## -remarks

You can only open silent AVI clips. <a href="/windows/desktop/Controls/acm-open">ACM_OPEN</a> and <a href="/windows/desktop/api/commctrl/nf-commctrl-animate_open">Animate_Open</a> will fail if <i>szName</i> specifies an AVI clip that contains sound. 

You can use <a href="/windows/desktop/api/commctrl/nf-commctrl-animate_close">Animate_Close</a> to close an AVI file or AVI resource that was previously opened for the specified animation control.
