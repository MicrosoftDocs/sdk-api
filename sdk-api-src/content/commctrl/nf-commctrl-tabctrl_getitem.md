---
UID: NF:commctrl.TabCtrl_GetItem
title: TabCtrl_GetItem macro (commctrl.h)
description: Retrieves information about a tab in a tab control. You can use this macro or send the TCM_GETITEM message explicitly.
helpviewer_keywords: ["TabCtrl_GetItem","TabCtrl_GetItem macro [Windows Controls]","_win32_TabCtrl_GetItem","_win32_TabCtrl_GetItem_cpp","commctrl/TabCtrl_GetItem","controls.TabCtrl_GetItem","controls._win32_TabCtrl_GetItem"]
old-location: controls\TabCtrl_GetItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_getitem.htm
ms.date: 10/21/2024
ms.keywords: TabCtrl_GetItem, TabCtrl_GetItem macro [Windows Controls], _win32_TabCtrl_GetItem, _win32_TabCtrl_GetItem_cpp, commctrl/TabCtrl_GetItem, controls.TabCtrl_GetItem, controls._win32_TabCtrl_GetItem
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
 - TabCtrl_GetItem
 - commctrl/TabCtrl_GetItem
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
 - TabCtrl_GetItem
---

# TabCtrl_GetItem macro

## -syntax

```cpp
BOOL TabCtrl_GetItem(
   HWND     hwnd,
   int      iItem,
   LPTCITEM pitem
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Retrieves information about a tab in a tab control. You can use this macro or send the <a href="/windows/desktop/Controls/tcm-getitem">TCM_GETITEM</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tab control.

### -param iItem

Type: <b>int</b>

Index of the tab.

### -param pitem

Type: <b>LPTCITEM</b>

Pointer to a <a href="/windows/desktop/api/commctrl/ns-commctrl-tcitema">TCITEM</a> structure that specifies the information to retrieve and receives information about the tab. When the message is sent, the 
					<b>mask</b> member specifies which attributes to return. If the <b>mask</b> member specifies the TCIF_TEXT value, the 
<b>pszText</b> member must contain the address of the buffer that receives the item text, and the <b>cchTextMax</b> member must specify the size of the buffer.

## -remarks

If the TCIF_TEXT flag is set in the 
				<b>mask</b> member of the <a href="/windows/desktop/api/commctrl/ns-commctrl-tcitema">TCITEM</a> structure, the control may change the <b>pszText</b> member of the structure to point to the new text instead of filling the buffer with the requested text. The control may set the <b>pszText</b> member to <b>NULL</b> to indicate that no text is associated with the item.
