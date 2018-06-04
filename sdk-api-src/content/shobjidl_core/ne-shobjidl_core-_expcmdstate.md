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

# _EXPCMDSTATE enumeration


## -description


<b>EXPCMDSTATE</b> values represent the command state of a Shell item.


## -enum-fields




### -field ECS_ENABLED

The item is enabled.


### -field ECS_DISABLED

The item is unavailable. It might be displayed to the user as a dimmed, inaccessible item.


### -field ECS_HIDDEN

The item is hidden.


### -field ECS_CHECKBOX

The item is displayed with a check box and that check box is not checked.


### -field ECS_CHECKED

The item is displayed with a check box and that check box is checked. <b>ECS_CHECKED</b> is always returned with ECS_CHECKBOX.


### -field ECS_RADIOCHECK

<b>Windows 7 and later</b>. The item is one of a group of mutually exclusive options selected through a radio button. ECS_RADIOCHECK does not imply that the item is the selected option, though it might be.


## -see-also




<a href="https://msdn.microsoft.com/bfc8b88b-0da2-46f6-b8c2-72f693ee1e7b">Button Types</a>



<a href="https://msdn.microsoft.com/bb600cb5-9b7e-45dc-beca-0a913c214084">IExplorerCommand::GetState</a>



<a href="https://msdn.microsoft.com/a93bc6af-bea3-48c1-b3bd-a2bb2a0582a7">IExplorerCommandState::GetState</a>
 

 

