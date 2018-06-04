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

# POST_UPGRADE_VERSION_INFO structure


## -description


Represents post-upgrade state information for the cluster service.


## -struct-fields




### -field newMajorVersion

The major version of the cluster service after the upgrade.


### -field newUpgradeVersion

The minor version of the cluster service after the update.


### -field oldMajorVersion

The major version of the cluster service before the upgrade.

<div class="alert"><b>Tip</b>  In some error conditions this field can be zero.</div>
<div> </div>

### -field oldUpgradeVersion

The minor version of the cluster service before the upgrade.

<div class="alert"><b>Tip</b>  In some error conditions this field can be zero.</div>
<div> </div>

### -field reserved

Reserved.


## -see-also




<a href="https://msdn.microsoft.com/9ab4b974-28b5-4f33-a7c4-b9b2472059aa">Resource DLL Structures</a>
 

 

