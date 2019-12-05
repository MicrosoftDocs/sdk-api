---
UID: NS:commctrl.tagLVITEMINDEX
title: LVITEMINDEX (commctrl.h)
description: Contains index information about a list-view item.
old-location: controls\LVITEMINDEX.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\lvitemindex.htm
ms.date: 12/05/2018
ms.keywords: '*PLVITEMINDEX, LVITEMINDEX, LVITEMINDEX structure [Windows Controls], PLVITEMINDEX, PLVITEMINDEX structure pointer [Windows Controls], _shell_LVITEMINDEX, _shell_LVITEMINDEX_cpp, commctrl/LVITEMINDEX, commctrl/PLVITEMINDEX, controls.LVITEMINDEX, controls._shell_LVITEMINDEX'
ms.topic: struct
f1_keywords:
- commctrl/LVITEMINDEX
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Commctrl.h
api_name:
- LVITEMINDEX
targetos: Windows
req.typenames: LVITEMINDEX, *PLVITEMINDEX
req.redist: 
ms.custom: 19H1
---

# LVITEMINDEX structure


## -description


Contains index information about a list-view item.


## -struct-fields




### -field iItem

Type: <b>int</b>

The index of the item.


### -field iGroup

Type: <b>int</b>

The index of the group the item belongs to.


## -remarks



This structure is used with the <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-listview_getitemindexrect">ListView_GetItemIndexRect</a>, <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-listview_getnextitemindex">ListView_GetNextItemIndex</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-listview_setitemindexstate">ListView_SetItemIndexState</a> macros. It is also used with the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-getitemindexrect">LVM_GETITEMINDEXRECT</a>, <a href="https://docs.microsoft.com/windows/desktop/controls/lvm-getnextitemindex">LVM_GETNEXTITEMINDEX</a>, and <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-setitemindexstate">LVM_SETITEMINDEXSTATE</a> messages.



