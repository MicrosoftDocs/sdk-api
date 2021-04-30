---
UID: NF:commctrl.ListView_SetToolTips
title: ListView_SetToolTips macro (commctrl.h)
description: Sets the tooltip control that the list-view control will use to display tooltips. You can use this macro or send the LVM_SETTOOLTIPS message explicitly.
helpviewer_keywords: ["ListView_SetToolTips","ListView_SetToolTips macro [Windows Controls]","_win32_ListView_SetToolTips","_win32_ListView_SetToolTips_cpp","commctrl/ListView_SetToolTips","controls.ListView_SetToolTips","controls._win32_ListView_SetToolTips"]
old-location: controls\ListView_SetToolTips.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_settooltips.htm
ms.date: 12/05/2018
ms.keywords: ListView_SetToolTips, ListView_SetToolTips macro [Windows Controls], _win32_ListView_SetToolTips, _win32_ListView_SetToolTips_cpp, commctrl/ListView_SetToolTips, controls.ListView_SetToolTips, controls._win32_ListView_SetToolTips
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
 - ListView_SetToolTips
 - commctrl/ListView_SetToolTips
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
 - ListView_SetToolTips
---

# ListView_SetToolTips macro


## -description

Sets the tooltip control that the list-view control will use to display tooltips. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-settooltips">LVM_SETTOOLTIPS</a> message explicitly.

## -parameters

### -param hwndLV

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param hwndNewHwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the tooltip control to be set.

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-listview_gettooltips">ListView_GetToolTips</a>