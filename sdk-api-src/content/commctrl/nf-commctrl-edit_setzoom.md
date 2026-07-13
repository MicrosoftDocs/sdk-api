---
UID: NF:commctrl.Edit_SetZoom
title: Edit_SetZoom macro (commctrl.h)
description: Sets the current zoom ratio of an edit control (the zoom ratio is always between 1/64 and 64). You can use this macro or send the EM_SETZOOM message explicitly.
helpviewer_keywords: ["Edit_SetZoom","Edit_SetZoom macro [Windows Controls]","commctrl/Edit_SetZoom","controls.edit_setzoom"]
old-location: controls\edit_setzoom.htm
tech.root: Controls
ms.assetid: 228EE5A0-AFAE-4485-8942-EB9BB6C12D54
ms.date: 07/01/2025
ms.keywords: Edit_SetZoom, Edit_SetZoom macro [Windows Controls], commctrl/Edit_SetZoom, controls.edit_setzoom
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
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
 - Edit_SetZoom
 - commctrl/Edit_SetZoom
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
 - Edit_SetZoom
---

# Edit_SetZoom macro

## -syntax

```cpp
void Edit_SetZoom(
         HWND hwndCtl,
  [out]  LONG numerator,
  [out]  LONG denominator
);
```


## -description



Sets the current zoom ratio of an edit control (the zoom ratio is always between 1/64 and 64). You can use this macro or send the <a href="/windows/desktop/Controls/em-setzoom">EM_SETZOOM</a> message explicitly.

## -parameters

### -param hwndCtl

A handle to the edit control.

### -param numerator [out]

The numerator of the ratio as a fraction.

### -param denominator [out]

The denominator of the ratio as a fraction.
