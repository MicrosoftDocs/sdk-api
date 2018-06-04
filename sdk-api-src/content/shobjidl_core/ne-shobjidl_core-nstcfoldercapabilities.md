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

# NSTCFOLDERCAPABILITIES enumeration


## -description


Specifies the state of a tree item. These values are used by methods of the <a href="https://msdn.microsoft.com/2a5580f6-42cb-46c7-9507-a59d36b2cd91">INameSpaceTreeControlFolderCapabilities</a> interface.


## -enum-fields




### -field NSTCFC_NONE

The property does not exist. Filtering is not supported.


### -field NSTCFC_PINNEDITEMFILTERING

Property exists. Supports filtering based on the value specified in <a href="https://msdn.microsoft.com/00937acb-1ce2-44f6-96a1-69e5dbb665f6">System.IsPinnedToNameSpaceTree</a>.


### -field NSTCFC_DELAY_REGISTER_NOTIFY

Delays registration for change notifications until the tree is expanded in the navigation pane.


## -remarks



The <b>NSTCFOLDERCAPABILITIES</b> type is defined in Shobjidl.h beginning in Windows 7.




## -see-also




<a href="https://msdn.microsoft.com/1534431c-21fc-4eb9-8f17-ddd7414bef94">INameSpaceTreeControlFolderCapabilities::GetFolderCapabilities</a>
 

 

