---
UID: NF:commctrl.TabCtrl_GetItemCount
title: TabCtrl_GetItemCount macro (commctrl.h)
description: Retrieves the number of tabs in the tab control. You can use this macro or send the TCM_GETITEMCOUNT message explicitly.
helpviewer_keywords: ["TabCtrl_GetItemCount","TabCtrl_GetItemCount macro [Windows Controls]","_win32_TabCtrl_GetItemCount","_win32_TabCtrl_GetItemCount_cpp","commctrl/TabCtrl_GetItemCount","controls.TabCtrl_GetItemCount","controls._win32_TabCtrl_GetItemCount"]
old-location: controls\TabCtrl_GetItemCount.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_getitemcount.htm
ms.date: 10/21/2024
ms.keywords: TabCtrl_GetItemCount, TabCtrl_GetItemCount macro [Windows Controls], _win32_TabCtrl_GetItemCount, _win32_TabCtrl_GetItemCount_cpp, commctrl/TabCtrl_GetItemCount, controls.TabCtrl_GetItemCount, controls._win32_TabCtrl_GetItemCount
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
 - TabCtrl_GetItemCount
 - commctrl/TabCtrl_GetItemCount
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
 - TabCtrl_GetItemCount
---

# TabCtrl_GetItemCount macro

## -syntax

```cpp
int TabCtrl_GetItemCount(
   HWND hwnd
);
```

## -returns

Type: **int**

Returns the number of items if successful, or zero otherwise.


## -description

Retrieves the number of tabs in the tab control. You can use this macro or send the <a href="/windows/desktop/Controls/tcm-getitemcount">TCM_GETITEMCOUNT</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tab control.
