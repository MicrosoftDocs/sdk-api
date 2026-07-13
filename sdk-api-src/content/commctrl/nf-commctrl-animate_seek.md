---
UID: NF:commctrl.Animate_Seek
title: Animate_Seek macro (commctrl.h)
description: Directs an animation control to display a particular frame of an AVI clip. The control displays the clip in the background while the thread continues executing. You can use this macro or send the ACM_PLAY message explicitly.
helpviewer_keywords: ["Animate_Seek","Animate_Seek macro [Windows Controls]","_win32_Animate_Seek","_win32_Animate_Seek_cpp","commctrl/Animate_Seek","controls.Animate_Seek","controls._win32_Animate_Seek"]
old-location: controls\Animate_Seek.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\animation\macros\animate_seek.htm
ms.date: 10/21/2024
ms.keywords: Animate_Seek, Animate_Seek macro [Windows Controls], _win32_Animate_Seek, _win32_Animate_Seek_cpp, commctrl/Animate_Seek, controls.Animate_Seek, controls._win32_Animate_Seek
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
 - Animate_Seek
 - commctrl/Animate_Seek
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
 - Animate_Seek
---

# Animate_Seek macro

## -syntax

```cpp
BOOL Animate_Seek(
   HWND hwnd,
   UINT frame
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns nonzero if successful, or zero otherwise.


## -description

Directs an animation control to display a particular frame of an AVI clip. The control displays the clip in the background while the thread continues executing. You can use this macro or send the <a href="/windows/desktop/Controls/acm-play">ACM_PLAY</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the animation control in which to display the AVI frame.

### -param frame

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The zero-based index of the frame to display.

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-animate_play">Animate_Play</a>
