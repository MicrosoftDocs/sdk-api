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

# IUpdate4::get_PerUser


## -description


Gets a Boolean value that indicates whether this is a per-user update.

This property is read-only.


## -parameters


## -remarks



Per-user updates are  designed to alter the current user’s environment only; not the environment of the machine as a whole. For example, an update which only alters files in the current user’s user directory could be a per-user update; an update which alters files in the Program Files directory or the Windows directory would not be a per-user update. Per-user updates are currently not processed by Automatic Updates or displayed in the Windows Update user interface. Instead, they are only available to callers who specifically request them in searches by using the <a href="https://msdn.microsoft.com/d37017d5-6f78-4b6c-ac0b-c83b83853079">IUpdateSearcher3</a> interface.  On computers running versions of Windows Update Agent that do not implement the <a href="https://msdn.microsoft.com/44904dd6-28d2-46b4-a237-0da68535cc84">IUpdate4</a> interface, only per-machine updates will be available; per-user updates will never be detected.




## -see-also




<a href="https://msdn.microsoft.com/44904dd6-28d2-46b4-a237-0da68535cc84">IUpdate4</a>
 

 

