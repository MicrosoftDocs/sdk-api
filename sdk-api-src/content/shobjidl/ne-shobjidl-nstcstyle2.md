---
UID: NE:shobjidl.NSTCSTYLE2
title: NSTCSTYLE2 (shobjidl.h)
description: Used by methods of the INameSpaceTreeControl2 to specify extended display styles in a Shell namespace treeview.
helpviewer_keywords: ["NSTCS2_DEFAULT","NSTCS2_DISPLAYPADDING","NSTCS2_DISPLAYPINNEDONLY","NSTCS2_INTERRUPTNOTIFICATIONS","NSTCS2_NOSINGLETONAUTOEXPAND","NSTCS2_SHOWNULLSPACEMENU","NSTCSTYLE2","NSTCSTYLE2 enumeration [Windows Shell]","NTSCS2_NEVERINSERTNONENUMERATED","_shell_NSTCSTYLE2","shell.NSTCSTYLE2","shobjidl/NSTCS2_DEFAULT","shobjidl/NSTCS2_DISPLAYPADDING","shobjidl/NSTCS2_DISPLAYPINNEDONLY","shobjidl/NSTCS2_INTERRUPTNOTIFICATIONS","shobjidl/NSTCS2_NOSINGLETONAUTOEXPAND","shobjidl/NSTCS2_SHOWNULLSPACEMENU","shobjidl/NSTCSTYLE2","shobjidl/NTSCS2_NEVERINSERTNONENUMERATED"]
old-location: shell\NSTCSTYLE2.htm
tech.root: shell
ms.assetid: 0bfa6900-71c0-44b7-8157-662bee58e6c9
ms.date: 12/05/2018
ms.keywords: NSTCS2_DEFAULT, NSTCS2_DISPLAYPADDING, NSTCS2_DISPLAYPINNEDONLY, NSTCS2_INTERRUPTNOTIFICATIONS, NSTCS2_NOSINGLETONAUTOEXPAND, NSTCS2_SHOWNULLSPACEMENU, NSTCSTYLE2, NSTCSTYLE2 enumeration [Windows Shell], NTSCS2_NEVERINSERTNONENUMERATED, _shell_NSTCSTYLE2, shell.NSTCSTYLE2, shobjidl/NSTCS2_DEFAULT, shobjidl/NSTCS2_DISPLAYPADDING, shobjidl/NSTCS2_DISPLAYPINNEDONLY, shobjidl/NSTCS2_INTERRUPTNOTIFICATIONS, shobjidl/NSTCS2_NOSINGLETONAUTOEXPAND, shobjidl/NSTCS2_SHOWNULLSPACEMENU, shobjidl/NSTCSTYLE2, shobjidl/NTSCS2_NEVERINSERTNONENUMERATED
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NSTCSTYLE2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NSTCSTYLE2
 - shobjidl/NSTCSTYLE2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shobjidl.h
api_name:
 - NSTCSTYLE2
---

# NSTCSTYLE2 enumeration


## -description

Used by methods of the <a href="/windows/desktop/api/shobjidl/nn-shobjidl-inamespacetreecontrol2">INameSpaceTreeControl2</a> to specify extended display styles in a Shell namespace treeview.

## -enum-fields

### -field NSTCS2_DEFAULT:0

Displays the tree nodes in default mode, which includes none of the following values.

### -field NSTCS2_INTERRUPTNOTIFICATIONS:0x1

Displays interrupt notifications.

### -field NSTCS2_SHOWNULLSPACEMENU:0x2

Displays the context menu in the padding space.

### -field NSTCS2_DISPLAYPADDING:0x4

Inserts spacing (padding) between top-level nodes.

### -field NSTCS2_DISPLAYPINNEDONLY:0x8

Filters items based on the <a href="/windows/desktop/properties/props-system-ispinnedtonamespacetree">System.IsPinnedToNameSpaceTree</a> value when <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrolfoldercapabilities">INameSpaceTreeControlFolderCapabilities</a> is implemented.

### -field NTSCS2_NOSINGLETONAUTOEXPAND:0x10

### -field NTSCS2_NEVERINSERTNONENUMERATED:0x20

Do not insert nonenumerated (SFGAO_NONENUMERATED) items in the tree.


#### - NSTCS2_NOSINGLETONAUTOEXPAND

Prevents automatic expansion of singleton nodes in the tree.

## -remarks

The value NSTCS2_ALLMASK can be used to mask for the NSTCS2_INTERRUPTNOTIFICATIONS, NSTCS2_SHOWNULLSPACEMENU, and NSTCS2_DISPLAYPADDING values.
