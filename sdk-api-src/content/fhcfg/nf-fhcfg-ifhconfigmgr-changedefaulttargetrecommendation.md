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

# IFhConfigMgr::ChangeDefaultTargetRecommendation


## -description


Causes the currently assigned backup target to be recommended or not recommended to other members of the home group that the computer belongs to.


## -parameters




### -param Recommend [in]

If set to <b>TRUE</b>, the currently assigned backup target is recommended to other members of the home group. If set to <b>FALSE</b> and the currently assigned backup target is currently recommended to other members of the home group, this recommendation is withdrawn.



## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code such as one of the values defined in the FhErrors.h header file.




## -remarks



When a backup target is recommended to other computers in the home group, users on those computers see that storage device in the list of available backup targets in the File History item in Control Panel. 

If the backup target is not recommended to other computers in the home group, or if the recommendation is withdrawn, the target does not appear in the list of available backup targets on the other computers.

A backup target cannot be recommended or not recommended on a computer that is joined to a domain or on a computer that is having ARM architecture.




## -see-also




<a href="https://msdn.microsoft.com/CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788">FhConfigMgr</a>



<a href="https://msdn.microsoft.com/CDE8A011-6E78-49DF-A5E1-8E968355BA11">IFhConfigMgr</a>
 

 

