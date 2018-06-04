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

# _OPM_ACP_PROTECTION_LEVEL enumeration


## -description


Specifies the protection level for Analog Copy Protection (ACP).


## -enum-fields




### -field OPM_ACP_OFF

ACP is disabled.


### -field OPM_ACP_LEVEL_ONE

ACP protection level 1.


### -field OPM_ACP_LEVEL_TWO

ACP protection level 2.


### -field OPM_ACP_LEVEL_THREE

ACP protection level 3.


### -field OPM_ACP_FORCE_ULONG

Reserved.


## -remarks



This enumeration is numerically equivalent to the <b>COPP_ACP_Protection_Level</b> enumeration used in Certified Output Protection Protocol. The OPM_ACP_OFF flag corresponds to COPP_ACP_Level0.




## -see-also




<a href="https://msdn.microsoft.com/e72e0a5e-476d-41f0-9139-54c4c488053f">OPM Enumerations</a>
 

 

