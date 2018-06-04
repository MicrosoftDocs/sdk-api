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

# GenTspecParms structure


## -description


The 
<b>GenTspecParms</b> structure stores generic Tspec parameters.


## -struct-fields




### -field TB_Tspec_r

Token bucket rate, in bytes per second.


### -field TB_Tspec_b

Token bucket depth, in bytes.


### -field TB_Tspec_p

Peak data rate, in bytes per second.


### -field TB_Tspec_m

Minimum policed unit, in bytes.


### -field TB_Tspec_M

Maximum packet size, in bytes.


## -see-also




<a href="https://msdn.microsoft.com/cefd94ed-ed54-471d-97fc-d523cedd71d6">GenTspec</a>



<a href="https://msdn.microsoft.com/c4244dba-237a-437b-94b7-fd814edb3506">IntServTspecBody</a>



<a href="https://msdn.microsoft.com/4e15b094-4250-4699-b66e-6734cf37cbb6">QualAppFlowSpec</a>



<a href="https://msdn.microsoft.com/dc22de18-3e9f-4b92-aba4-579aa47fab64">QualTspec</a>



<a href="https://msdn.microsoft.com/f9afa6f9-1de7-469e-a317-2dea98c8291c">QualTspecParms</a>



<a href="https://msdn.microsoft.com/d7905687-1af8-4469-b8de-a2445afa90f4">SENDER_TSPEC</a>
 

 

