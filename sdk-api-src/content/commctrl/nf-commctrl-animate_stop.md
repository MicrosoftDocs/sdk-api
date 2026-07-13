---
UID: NF:commctrl.Animate_Stop
title: Animate_Stop macro (commctrl.h)
description: Stops playing an AVI clip in an animation control. You can use this macro or send the ACM_STOP message explicitly.
helpviewer_keywords: ["Animate_Stop","Animate_Stop macro [Windows Controls]","_win32_Animate_Stop","_win32_Animate_Stop_cpp","commctrl/Animate_Stop","controls.Animate_Stop","controls._win32_Animate_Stop"]
old-location: controls\Animate_Stop.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\animation\macros\animate_stop.htm
ms.date: 10/21/2024
ms.keywords: Animate_Stop, Animate_Stop macro [Windows Controls], _win32_Animate_Stop, _win32_Animate_Stop_cpp, commctrl/Animate_Stop, controls.Animate_Stop, controls._win32_Animate_Stop
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
 - Animate_Stop
 - commctrl/Animate_Stop
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
 - Animate_Stop
---

# Animate_Stop macro

## -syntax

```cpp
BOOL Animate_Stop(
   HWND hwnd
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns nonzero if successful, or zero otherwise.


## -description

Stops playing an AVI clip in an animation control. You can use this macro or send the <a href="/windows/desktop/Controls/acm-stop">ACM_STOP</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the animation control.
