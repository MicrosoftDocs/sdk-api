---
UID: NF:commctrl.TabCtrl_SetImageList
title: TabCtrl_SetImageList macro (commctrl.h)
description: Assigns an image list to a tab control. You can use this macro or send the TCM_SETIMAGELIST message explicitly.
helpviewer_keywords: ["TabCtrl_SetImageList","TabCtrl_SetImageList macro [Windows Controls]","_win32_TabCtrl_SetImageList","_win32_TabCtrl_SetImageList_cpp","commctrl/TabCtrl_SetImageList","controls.TabCtrl_SetImageList","controls._win32_TabCtrl_SetImageList"]
old-location: controls\TabCtrl_SetImageList.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_setimagelist.htm
ms.date: 10/21/2024
ms.keywords: TabCtrl_SetImageList, TabCtrl_SetImageList macro [Windows Controls], _win32_TabCtrl_SetImageList, _win32_TabCtrl_SetImageList_cpp, commctrl/TabCtrl_SetImageList, controls.TabCtrl_SetImageList, controls._win32_TabCtrl_SetImageList
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
 - TabCtrl_SetImageList
 - commctrl/TabCtrl_SetImageList
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
 - TabCtrl_SetImageList
---

# TabCtrl_SetImageList macro

## -syntax

```cpp
BOOL TabCtrl_SetImageList(
   HWND       hwnd,
   HIMAGELIST himl
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns the handle to the previous image list, or <b>NULL</b> if there is no previous image list.


## -description

Assigns an image list to a tab control. You can use this macro or send the <a href="/windows/desktop/Controls/tcm-setimagelist">TCM_SETIMAGELIST</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tab control.

### -param himl

Type: <b>HIMAGELIST</b>

Handle to the image list to assign to the tab control.
