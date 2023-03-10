---
UID: NS:commctrl.LVINSERTMARK
title: LVINSERTMARK (commctrl.h)
description: Used to describe insertion points.
helpviewer_keywords: ["*LPLVINSERTMARK","LVIM_AFTER","LVINSERTMARK","LVINSERTMARK structure [Windows Controls]","PLVINSERTMARK","PLVINSERTMARK structure pointer [Windows Controls]","commctrl/LVINSERTMARK","commctrl/PLVINSERTMARK","controls.LVINSERTMARK","controls.inet_LVINSERTMARK","inet_LVINSERTMARK","inet_LVINSERTMARK_cpp"]
old-location: controls\LVINSERTMARK.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\lvinsertmark.htm
ms.date: 12/05/2018
ms.keywords: '*LPLVINSERTMARK, LVIM_AFTER, LVINSERTMARK, LVINSERTMARK structure [Windows Controls], PLVINSERTMARK, PLVINSERTMARK structure pointer [Windows Controls], commctrl/LVINSERTMARK, commctrl/PLVINSERTMARK, controls.LVINSERTMARK, controls.inet_LVINSERTMARK, inet_LVINSERTMARK, inet_LVINSERTMARK_cpp'
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
req.typenames: LVINSERTMARK, *LPLVINSERTMARK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPLVINSERTMARK
 - commctrl/LPLVINSERTMARK
 - LVINSERTMARK
 - commctrl/LVINSERTMARK
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
 - LVINSERTMARK
---

# LVINSERTMARK structure


## -description

Used to describe insertion points.

## -struct-fields

### -field cbSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size of the <b>LVINSERTMARK</b> structure.

### -field dwFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Flag that specifies where the insertion point should appear. Use the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LVIM_AFTER"></a><a id="lvim_after"></a><dl>
<dt><b>LVIM_AFTER</b></dt>
</dl>
</td>
<td width="60%">
The insertion point appears after the item specified if the LVIM_AFTER flag is set; otherwise it appears before the specified item.

</td>
</tr>
</table>

### -field iItem

Type: <b>int</b>

Item next to which the insertion point appears. If this member contains -1, there is no insertion point.

### -field dwReserved

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

