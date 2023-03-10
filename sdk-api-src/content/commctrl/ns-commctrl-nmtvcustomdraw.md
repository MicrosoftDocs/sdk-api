---
UID: NS:commctrl.tagNMTVCUSTOMDRAW
title: NMTVCUSTOMDRAW (commctrl.h)
description: Contains information specific to an NM_CUSTOMDRAW (tree view) notification code sent by a tree-view control.
helpviewer_keywords: ["*LPNMTVCUSTOMDRAW","LPNMTVCUSTOMDRAW","LPNMTVCUSTOMDRAW structure pointer [Windows Controls]","NMTVCUSTOMDRAW","NMTVCUSTOMDRAW structure [Windows Controls]","_win32_NMTVCUSTOMDRAW","_win32_NMTVCUSTOMDRAW_cpp","commctrl/LPNMTVCUSTOMDRAW","commctrl/NMTVCUSTOMDRAW","controls.NMTVCUSTOMDRAW","controls._win32_NMTVCUSTOMDRAW"]
old-location: controls\NMTVCUSTOMDRAW.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\structures\nmtvcustomdraw.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMTVCUSTOMDRAW, LPNMTVCUSTOMDRAW, LPNMTVCUSTOMDRAW structure pointer [Windows Controls], NMTVCUSTOMDRAW, NMTVCUSTOMDRAW structure [Windows Controls], _win32_NMTVCUSTOMDRAW, _win32_NMTVCUSTOMDRAW_cpp, commctrl/LPNMTVCUSTOMDRAW, commctrl/NMTVCUSTOMDRAW, controls.NMTVCUSTOMDRAW, controls._win32_NMTVCUSTOMDRAW'
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
req.typenames: NMTVCUSTOMDRAW, *LPNMTVCUSTOMDRAW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMTVCUSTOMDRAW
 - commctrl/tagNMTVCUSTOMDRAW
 - LPNMTVCUSTOMDRAW
 - commctrl/LPNMTVCUSTOMDRAW
 - NMTVCUSTOMDRAW
 - commctrl/NMTVCUSTOMDRAW
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
 - NMTVCUSTOMDRAW
---

# NMTVCUSTOMDRAW structure


## -description

Contains information specific to an <a href="/windows/desktop/Controls/nm-customdraw-tree-view">NM_CUSTOMDRAW (tree view)</a> notification code sent by a tree-view control.

## -struct-fields

### -field nmcd

Type: <b><a href="/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw">NMCUSTOMDRAW</a></b>


<a href="/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw">NMCUSTOMDRAW</a> structure that contains general custom draw information.

### -field clrText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>


<a href="/windows/desktop/gdi/colorref">COLORREF</a> value representing the color that will be used to display text foreground in the tree-view control.

### -field clrTextBk

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>


<a href="/windows/desktop/gdi/colorref">COLORREF</a> value representing the color that will be used to display text background in the tree-view control.

### -field iLevel

Type: <b>int</b>


<a href="/windows/desktop/Controls/common-control-versions">Version 4.71</a>. Zero-based level of the item being drawn. The root item is at level zero, a child of the root item is at level one, and so on.