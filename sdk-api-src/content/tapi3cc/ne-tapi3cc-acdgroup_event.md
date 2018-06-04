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

# ACDGROUP_EVENT enumeration


## -description


The 
<b>ACDGROUP_EVENT</b> enum describes ACD group events. The 
<a href="https://msdn.microsoft.com/9bc67911-cfb6-450c-bdc6-ade8d4617271">ITACDGroupEvent::get_Event</a> method returns a member of this enum to indicate the type of ACD group event that occurred.


## -enum-fields




### -field ACDGE_NEW_GROUP

A new ACD group has been added.


### -field ACDGE_GROUP_REMOVED

An ACD group has been removed.


## -see-also




<a href="https://msdn.microsoft.com/9bc67911-cfb6-450c-bdc6-ade8d4617271">ITACDGroupEvent::get_Event</a>
 

 

