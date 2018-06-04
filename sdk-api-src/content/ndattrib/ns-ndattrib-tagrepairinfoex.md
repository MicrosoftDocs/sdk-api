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

# tagRepairInfoEx structure


## -description


Contains detailed repair information that can be used to help resolve the  root cause of an incident.


## -struct-fields




### -field repair

Type: <b><a href="https://msdn.microsoft.com/07639ac5-e586-4ab1-96e8-502c378de940">RepairInfo</a></b>

The detailed repair information. 


### -field repairRank

Type: <b>USHORT</b>

The rank of the repair, relative to other repairs in the <a href="https://msdn.microsoft.com/01d02658-ae12-4465-94fc-7a966dcdd8fb">RootCauseInfo</a> structure associated with the incident. A repair with rank 1 is expected to be more relevant to the problem and thus will be the first repair to be attempted. The success of any individual repair is not guaranteed, regardless of its rank.


## -see-also




<a href="https://msdn.microsoft.com/b4e3e758-88cd-4ce2-b1a4-5b47889aae9b">FreeRepairInfoExs</a>



<a href="https://msdn.microsoft.com/07639ac5-e586-4ab1-96e8-502c378de940">RepairInfo</a>



<a href="https://msdn.microsoft.com/01d02658-ae12-4465-94fc-7a966dcdd8fb">RootCauseInfo</a>
 

 

