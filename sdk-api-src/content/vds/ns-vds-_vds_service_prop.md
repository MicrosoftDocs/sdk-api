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

# _VDS_SERVICE_PROP structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the properties of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff597669">service object</a>.


## -struct-fields




### -field pwszVersion

The version of VDS; a zero-terminated, human-readable string.


### -field ulFlags

A bitmask of <a href="https://msdn.microsoft.com/d14718bd-43a3-4775-a218-27c59f6995eb">VDS_SERVICE_FLAG</a> enumeration values that describe the service.


## -remarks



 The <a href="https://msdn.microsoft.com/fb5fe743-4833-400a-a8aa-8de886203190">IVdsService::GetProperties</a>
      method returns this structure to report the properties of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff597669">service object</a>.




## -see-also




<a href="https://msdn.microsoft.com/fb5fe743-4833-400a-a8aa-8de886203190">IVdsService::GetProperties</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>
 

 

