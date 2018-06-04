---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



