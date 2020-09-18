---
UID: NS:commctrl.tagLVTILEINFO
title: LVTILEINFO (commctrl.h)
description: Provides information about an item in a list-view control when it is displayed in tile view.
helpviewer_keywords: ["*PLVTILEINFO","LVTILEINFO","LVTILEINFO structure [Windows Controls]","PLVTILEINFO","PLVTILEINFO structure pointer [Windows Controls]","commctrl/LVTILEINFO","commctrl/PLVTILEINFO","controls.LVTILEINFO","controls.inet_LVTILEINFO","inet_LVTILEINFO","inet_LVTILEINFO_cpp"]
old-location: controls\LVTILEINFO.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\lvtileinfo.htm
ms.date: 12/05/2018
ms.keywords: '*PLVTILEINFO, LVTILEINFO, LVTILEINFO structure [Windows Controls], PLVTILEINFO, PLVTILEINFO structure pointer [Windows Controls], commctrl/LVTILEINFO, commctrl/PLVTILEINFO, controls.LVTILEINFO, controls.inet_LVTILEINFO, inet_LVTILEINFO, inet_LVTILEINFO_cpp'
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
req.typenames: LVTILEINFO, *PLVTILEINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagLVTILEINFO
 - commctrl/tagLVTILEINFO
 - PLVTILEINFO
 - commctrl/PLVTILEINFO
 - LVTILEINFO
 - commctrl/LVTILEINFO
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
 - LVTILEINFO
---

# LVTILEINFO structure


## -description

Provides information about an item in a list-view control when it is displayed in tile view.

## -struct-fields

### -field cbSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The size of the <b>LVTILEINFO</b> structure.

### -field iItem

Type: <b>int</b>

The item for which the information is retrieved or set.

### -field cColumns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of data columns displayed for this item. When retrieving information, initialize this value to the size of the <b>puColumns</b> array. On return, the member is set to the number of columns actually set for the item.

### -field puColumns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">PUINT</a></b>

A pointer to an array of column indices, specifying which columns are displayed for this item, and the order of those columns. When retrieving information, allocate an array large enough to hold the greatest number of columns expected.

### -field piColFmt

Type: <b>int*</b>

A pointer to an array of column formats (for example, LVCFMT_LEFT), one for each of the columns specified in <b>puColumns</b>. When retrieving information, allocate an array large enough to hold the greatest number of column formats expected.

## -remarks

In tile view, the item name is displayed to the right of the icon. You can specify additional subitems (corresponding to columns in the details view), to be displayed on lines below the item name. The <b>puColumns</b> array contains the indices of subitems to be displayed. Indices should be greater than 0, because subitem 0, the item name, is already displayed.

Column information can also be set in the <a href="/windows/desktop/api/commctrl/ns-commctrl-lvitema">LVITEM</a> structure when creating the list item.