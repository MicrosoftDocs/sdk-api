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

# _VSS_ROLLFORWARD_TYPE enumeration


## -description


The <b>VSS_ROLLFORWARD_TYPE</b> enumeration is used by a 
    requester to indicate the type of roll-forward operation it is about to perform.


## -enum-fields




### -field VSS_RF_UNDEFINED

No roll-forward type is defined. 
      

This indicates an error on the part of the requester.


### -field VSS_RF_NONE

The roll-forward operation should not roll forward through logs.


### -field VSS_RF_ALL

The roll-forward operation should roll forward through all logs.


### -field VSS_RF_PARTIAL

The roll-forward operation should roll forward through logs up to a specified restore point.


## -remarks



A requester sets the roll-forward operation type and specifies the restore point for partial roll-forward operations using 
    <a href="https://msdn.microsoft.com/9529284f-2150-4d32-af6c-178ba8681945">IVssBackupComponentsEx2::SetRollForward</a>.




## -see-also




<a href="https://msdn.microsoft.com/9529284f-2150-4d32-af6c-178ba8681945">IVssBackupComponentsEx2::SetRollForward</a>
 

 

