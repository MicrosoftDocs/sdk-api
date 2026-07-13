---
UID: NF:commctrl.ListView_CancelEditLabel
title: ListView_CancelEditLabel macro (commctrl.h)
description: Cancels an item text editing operation. You can use this macro or send the LVM_CANCELEDITLABEL message explicitly.
helpviewer_keywords: ["ListView_CancelEditLabel","ListView_CancelEditLabel macro [Windows Controls]","_win32_ListView_CancelEditLabel","_win32_ListView_CancelEditLabel_cpp","commctrl/ListView_CancelEditLabel","controls.ListView_CancelEditLabel","controls._win32_ListView_CancelEditLabel"]
old-location: controls\ListView_CancelEditLabel.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_canceleditlabel.htm
ms.date: 10/21/2024
ms.keywords: ListView_CancelEditLabel, ListView_CancelEditLabel macro [Windows Controls], _win32_ListView_CancelEditLabel, _win32_ListView_CancelEditLabel_cpp, commctrl/ListView_CancelEditLabel, controls.ListView_CancelEditLabel, controls._win32_ListView_CancelEditLabel
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
 - ListView_CancelEditLabel
 - commctrl/ListView_CancelEditLabel
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
 - ListView_CancelEditLabel
---

# ListView_CancelEditLabel macro

## -syntax

```cpp
void ListView_CancelEditLabel(
   HWND hwnd
);
```


## -description

Cancels an item text editing operation. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-canceleditlabel">LVM_CANCELEDITLABEL</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

## -remarks

To use <b>ListView_CancelEditLabel</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
