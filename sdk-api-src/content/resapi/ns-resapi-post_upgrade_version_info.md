---
UID: NS:resapi.POST_UPGRADE_VERSION_INFO
title: POST_UPGRADE_VERSION_INFO (resapi.h)
author: windows-sdk-content
description: Represents post-upgrade state information for the cluster service.
old-location: mscs\post_upgrade_version_info.htm
tech.root: MsCS
ms.assetid: 6F5DE9C6-5499-49FE-99D1-C8B8AE88CB18
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PPOST_UPGRADE_VERSION_INFO, POST_UPGRADE_VERSION_INFO, POST_UPGRADE_VERSION_INFO structure [Failover Cluster], PPOST_UPGRADE_VERSION_INFO, PPOST_UPGRADE_VERSION_INFO structure pointer [Failover Cluster], mscs.post_upgrade_version_info, resapi/POST_UPGRADE_VERSION_INFO, resapi/PPOST_UPGRADE_VERSION_INFO"
ms.topic: struct
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ResApi.h
api_name:
 - POST_UPGRADE_VERSION_INFO
product: Windows
targetos: Windows
req.typenames: POST_UPGRADE_VERSION_INFO, *PPOST_UPGRADE_VERSION_INFO
req.redist: 
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
 

 

