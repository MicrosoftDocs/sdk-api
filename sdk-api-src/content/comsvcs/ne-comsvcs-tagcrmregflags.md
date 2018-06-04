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

# tagCRMREGFLAGS enumeration


## -description


Controls which phases of transaction completion should be received by the CRM compensator and whether recovery should fail if in-doubt transactions remain after recovery has been attempted.


## -enum-fields




### -field CRMREGFLAG_PREPAREPHASE

Receive the prepare phase.


### -field CRMREGFLAG_COMMITPHASE

Receive the commit phase.


### -field CRMREGFLAG_ABORTPHASE

Receive the abort phase.


### -field CRMREGFLAG_ALLPHASES

Receive all phases.


### -field CRMREGFLAG_FAILIFINDOUBTSREMAIN

Fail if in-doubt transactions remain after recovery.


## -see-also




<a href="https://msdn.microsoft.com/f7907dff-a4a1-4526-8dab-547e819199ec">ICrmLogControl::RegisterCompensator</a>
 

 

