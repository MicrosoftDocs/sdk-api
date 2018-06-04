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

# _VSS_RECOVERY_OPTIONS enumeration


## -description


Used by a requester to specify how a resynchronization operation is to be performed.


## -enum-fields




### -field VSS_RECOVERY_REVERT_IDENTITY_ALL

 After the resynchronization operation is complete, the signature of each target LUN  should be identical to that of the original LUN that was used to create the shadow copy.


### -field VSS_RECOVERY_NO_VOLUME_CHECK

Volume safety checks should not be performed.


## -see-also




<a href="https://msdn.microsoft.com/2e468527-11e7-42d8-808b-2cb2eb86e0ba">IVssBackupComponentsEx3::RecoverSet</a>
 

 

