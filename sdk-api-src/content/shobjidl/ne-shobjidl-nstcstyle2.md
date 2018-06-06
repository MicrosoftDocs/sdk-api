---
UID: NE:shobjidl.NSTCSTYLE2
title: NSTCSTYLE2
author: windows-sdk-content
description: Used by methods of the INameSpaceTreeControl2 to specify extended display styles in a Shell namespace treeview.
old-location: shell\NSTCSTYLE2.htm
old-project: shell
ms.assetid: 0bfa6900-71c0-44b7-8157-662bee58e6c9
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: NSTCS2_DEFAULT, NSTCS2_DISPLAYPADDING, NSTCS2_DISPLAYPINNEDONLY, NSTCS2_INTERRUPTNOTIFICATIONS, NSTCS2_NOSINGLETONAUTOEXPAND, NSTCS2_SHOWNULLSPACEMENU, NSTCSTYLE2, NSTCSTYLE2 enumeration [Windows Shell], NTSCS2_NEVERINSERTNONENUMERATED, _shell_NSTCSTYLE2, shell.NSTCSTYLE2, shobjidl/NSTCS2_DEFAULT, shobjidl/NSTCS2_DISPLAYPADDING, shobjidl/NSTCS2_DISPLAYPINNEDONLY, shobjidl/NSTCS2_INTERRUPTNOTIFICATIONS, shobjidl/NSTCS2_NOSINGLETONAUTOEXPAND, shobjidl/NSTCS2_SHOWNULLSPACEMENU, shobjidl/NSTCSTYLE2, shobjidl/NTSCS2_NEVERINSERTNONENUMERATED
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: NSTCSTYLE2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shobjidl.h
api_name:
 - NSTCSTYLE2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# NSTCSTYLE2 enumeration


## -description


Used by methods of the <a href="https://msdn.microsoft.com/5f9514db-35fe-44c7-9324-d69022628913">INameSpaceTreeControl2</a> to specify extended display styles in a Shell namespace treeview.


## -enum-fields




### -field NSTCS2_DEFAULT

Displays the tree nodes in default mode, which includes none of the following values.


### -field NSTCS2_INTERRUPTNOTIFICATIONS

Displays interrupt notifications.


### -field NSTCS2_SHOWNULLSPACEMENU

Displays the context menu in the padding space.


### -field NSTCS2_DISPLAYPADDING

Inserts spacing (padding) between top-level nodes.


### -field NSTCS2_DISPLAYPINNEDONLY

Filters items based on the <a href="https://msdn.microsoft.com/00937acb-1ce2-44f6-96a1-69e5dbb665f6">System.IsPinnedToNameSpaceTree</a> value when <a href="https://msdn.microsoft.com/2a5580f6-42cb-46c7-9507-a59d36b2cd91">INameSpaceTreeControlFolderCapabilities</a> is implemented.


### -field NTSCS2_NOSINGLETONAUTOEXPAND


### -field NTSCS2_NEVERINSERTNONENUMERATED

Do not insert nonenumerated (SFGAO_NONENUMERATED) items in the tree.


#### - NSTCS2_NOSINGLETONAUTOEXPAND

Prevents automatic expansion of singleton nodes in the tree.


## -remarks



The value NSTCS2_ALLMASK can be used to mask for the NSTCS2_INTERRUPTNOTIFICATIONS, NSTCS2_SHOWNULLSPACEMENU, and NSTCS2_DISPLAYPADDING values.



