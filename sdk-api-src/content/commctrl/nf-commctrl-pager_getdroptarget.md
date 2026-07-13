---
UID: NF:commctrl.Pager_GetDropTarget
title: Pager_GetDropTarget macro (commctrl.h)
description: Retrieves a pager control's IDropTarget interface pointer. You can use this macro or send the PGM_GETDROPTARGET message explicitly.
helpviewer_keywords: ["Pager_GetDropTarget","Pager_GetDropTarget macro [Windows Controls]","_win32_Pager_GetDropTarget","_win32_Pager_GetDropTarget_cpp","commctrl/Pager_GetDropTarget","controls.Pager_GetDropTarget","controls._win32_Pager_GetDropTarget"]
old-location: controls\Pager_GetDropTarget.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\pager\macros\pager_getdroptarget.htm
ms.date: 10/21/2024
ms.keywords: Pager_GetDropTarget, Pager_GetDropTarget macro [Windows Controls], _win32_Pager_GetDropTarget, _win32_Pager_GetDropTarget_cpp, commctrl/Pager_GetDropTarget, controls.Pager_GetDropTarget, controls._win32_Pager_GetDropTarget
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
 - Pager_GetDropTarget
 - commctrl/Pager_GetDropTarget
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
 - Pager_GetDropTarget
---

# Pager_GetDropTarget macro

## -syntax

```cpp
void Pager_GetDropTarget(
   HWND        hwnd,
   IDropTarget **ppdt
);
```


## -description

Retrieves a pager control's <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a> interface pointer. You can use this macro or send the <a href="/windows/desktop/Controls/pgm-getdroptarget">PGM_GETDROPTARGET</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the pager control.

### -param ppdt

Type: <b><a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a>**</b>

Pointer to an <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a> pointer that receives the interface pointer. It is the caller's responsibility to call 
					<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on this pointer when it is no longer needed.
