---
UID: NF:commctrl.ListView_GetFooterInfo
title: ListView_GetFooterInfo macro (commctrl.h)
description: Gets information on the footer of a specified list-view control. Use this macro or send the LVM_GETFOOTERINFO message explicitly.
helpviewer_keywords: ["ListView_GetFooterInfo","ListView_GetFooterInfo macro [Windows Controls]","_shell_ListView_GetFooterInfo","_shell_ListView_GetFooterInfo_cpp","commctrl/ListView_GetFooterInfo","controls.ListView_GetFooterInfo","controls._shell_ListView_GetFooterInfo"]
old-location: controls\ListView_GetFooterInfo.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getfooterinfo.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetFooterInfo, ListView_GetFooterInfo macro [Windows Controls], _shell_ListView_GetFooterInfo, _shell_ListView_GetFooterInfo_cpp, commctrl/ListView_GetFooterInfo, controls.ListView_GetFooterInfo, controls._shell_ListView_GetFooterInfo
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
 - ListView_GetFooterInfo
 - commctrl/ListView_GetFooterInfo
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
 - ListView_GetFooterInfo
---

# ListView_GetFooterInfo macro

## -syntax

```cpp
BOOL ListView_GetFooterInfo(
  [in]      HWND           hwnd,
  [in, out] LPLVFOOTERINFO plvfi
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b>.


## -description

Gets information on the footer of a specified list-view control. Use this macro or send the <a href="/windows/desktop/Controls/lvm-getfooterinfo">LVM_GETFOOTERINFO</a> message explicitly.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param plvfi [in, out]

Type: <b>LPLVFOOTERINFO</b>

A pointer to a <a href="/windows/desktop/api/commctrl/ns-commctrl-lvfooterinfo">LVFOOTERINFO</a> structure to receive information depending on the value of the <b>mask</b> member. The calling application is responsible for allocating this structure and setting the <b>mask</b> member.
