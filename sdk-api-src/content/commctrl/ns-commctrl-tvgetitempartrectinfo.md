---
UID: NS:commctrl.tagTVGETITEMPARTRECTINFO
title: TVGETITEMPARTRECTINFO (commctrl.h)
description: Contains information for identifying the &quot;hit zone&quot; for a specified part of a tree item. The structure is used with the TVM_GETITEMPARTRECT message and the TreeView_GetItemPartRect macro.
helpviewer_keywords: ["TVGETITEMPARTRECTINFO","TVGETITEMPARTRECTINFO structure [Windows Controls]","_shell_TVGETITEMPARTRECTINFO","_shell_TVGETITEMPARTRECTINFO_cpp","commctrl/TVGETITEMPARTRECTINFO","controls.TVGETITEMPARTRECTINFO","controls._shell_TVGETITEMPARTRECTINFO"]
old-location: controls\TVGETITEMPARTRECTINFO.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\structures\tvgetitempartrectinfo.htm
ms.date: 12/05/2018
ms.keywords: TVGETITEMPARTRECTINFO, TVGETITEMPARTRECTINFO structure [Windows Controls], _shell_TVGETITEMPARTRECTINFO, _shell_TVGETITEMPARTRECTINFO_cpp, commctrl/TVGETITEMPARTRECTINFO, controls.TVGETITEMPARTRECTINFO, controls._shell_TVGETITEMPARTRECTINFO
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
req.typenames: TVGETITEMPARTRECTINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagTVGETITEMPARTRECTINFO
 - commctrl/tagTVGETITEMPARTRECTINFO
 - TVGETITEMPARTRECTINFO
 - commctrl/TVGETITEMPARTRECTINFO
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
 - TVGETITEMPARTRECTINFO
---

# TVGETITEMPARTRECTINFO structure


## -description

Contains information for identifying the "hit zone" for a specified part of a tree item. The structure is used with the <a href="/windows/desktop/Controls/tvm-getitempartrect">TVM_GETITEMPARTRECT</a> message and the <a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_getitempartrect">TreeView_GetItemPartRect</a> macro.

## -struct-fields

### -field hti

Type: <b>HTREEITEM</b>

Handle to the parent item.

### -field prc

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure to receive the coordinates of the bounding rectangle. The sender of the message (the caller) is responsible for allocating this structure.

### -field partID

Type: <b>TVITEMPART</b>

ID of the item part. This value must be <b>TVGIPR_BUTTON</b> (0x0001).