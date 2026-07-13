---
UID: NF:commctrl.Animate_IsPlaying
title: Animate_IsPlaying macro (commctrl.h)
description: Checks to see if an Audio-Video Interleaved (AVI) clip is playing. You can use this macro or send an ACM_ISPLAYING message.
helpviewer_keywords: ["Animate_IsPlaying","Animate_IsPlaying macro [Windows Controls]","_shell_Animate_IsPlaying","_shell_Animate_IsPlaying_cpp","commctrl/Animate_IsPlaying","controls.Animate_IsPlaying","controls._shell_Animate_IsPlaying"]
old-location: controls\Animate_IsPlaying.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\animation\macros\animate_isplaying.htm
ms.date: 10/21/2024
ms.keywords: Animate_IsPlaying, Animate_IsPlaying macro [Windows Controls], _shell_Animate_IsPlaying, _shell_Animate_IsPlaying_cpp, commctrl/Animate_IsPlaying, controls.Animate_IsPlaying, controls._shell_Animate_IsPlaying
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
 - Animate_IsPlaying
 - commctrl/Animate_IsPlaying
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
 - Animate_IsPlaying
---

# Animate_IsPlaying macro

## -syntax

```cpp
BOOL Animate_IsPlaying(
   HWND hwnd
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns nonzero if successful, or zero otherwise.


## -description

Checks to see if an Audio-Video Interleaved (AVI) clip is playing. You can use this macro or send an <a href="/windows/desktop/Controls/acm-isplaying">ACM_ISPLAYING</a> message.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the animation control.
