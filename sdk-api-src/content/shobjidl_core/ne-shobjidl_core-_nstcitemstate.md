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

# _NSTCITEMSTATE enumeration


## -description


Specifies the state of a tree item. These values are used by methods of the <a href="https://msdn.microsoft.com/2072cb3c-e540-4708-bfe8-33fff3a190bd">INameSpaceTreeControl</a> interface.


## -enum-fields




### -field NSTCIS_NONE

The item has default state; it is not selected, expanded, bolded or disabled.


### -field NSTCIS_SELECTED

The item is selected.


### -field NSTCIS_EXPANDED

The item is expanded.


### -field NSTCIS_BOLD

The item is bold.


### -field NSTCIS_DISABLED

The item is disabled.


### -field NSTCIS_SELECTEDNOEXPAND

<b>Windows 7 and later</b>. The item is selected, but not expanded.


## -see-also




<a href="https://msdn.microsoft.com/78bee2db-6a28-4fcb-9c43-ab411196ab04">INameSpaceTreeControl::GetItemState</a>



<a href="https://msdn.microsoft.com/f57c5abc-0803-409d-9938-3826f9d8058d">INameSpaceTreeControl::SetItemState</a>
 

 

