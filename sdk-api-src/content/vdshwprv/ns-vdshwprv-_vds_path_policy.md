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

# _VDS_PATH_POLICY structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the 
    load balance policy as it applies to a particular path.


## -struct-fields




### -field pathId

The ID of the path used by MPIO.


### -field bPrimaryPath

If set, indicates that the path is a primary path for MPIO.


### -field ulWeight

The weight assigned to the path. This is only relevant if the load balance policy for the LUN is 
      <b>VDS_LBP_WEIGHTED_PATHS</b>.


## -see-also




<a href="https://msdn.microsoft.com/56866ecb-c84b-4297-9bd4-54969501bf9e">IVdsLunMpio::GetLoadBalancePolicy</a>



<a href="https://msdn.microsoft.com/2f3eb00a-864e-4fb7-a722-4537e6b8dd42">IVdsLunMpio::SetLoadBalancePolicy</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>
 

 

