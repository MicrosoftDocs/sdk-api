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

# _MC_VCP_CODE_TYPE enumeration


## -description



        Describes a Virtual Control Panel (VCP) code type.


## -enum-fields




### -field MC_MOMENTARY


            Momentary VCP code. Sending a command of this type causes the monitor to initiate a self-timed operation and then revert to its original state. Examples include display tests and degaussing.
          


### -field MC_SET_PARAMETER


            Set Parameter VCP code. Sending a command of this type changes some aspect of the monitor's operation.
          


## -see-also




<a href="https://msdn.microsoft.com/b0b06137-8f67-46fc-ba6b-3022f3331fa5">GetVCPFeatureAndVCPFeatureReply</a>



<a href="https://msdn.microsoft.com/d6ab74af-0ac4-4dfe-bbf8-21b8339d2826">Monitor Configuration Enumeration Types</a>



<a href="https://msdn.microsoft.com/0c3acb13-c5db-44ce-937d-b0b001a08062">SetMonitorDisplayAreaSize</a>
 

 

