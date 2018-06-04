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

# _SERVICE_TYPE enumeration


## -description


The values of the 
<b>SERVICE_TYPE</b> enumeration type specify the type of service administered from the SDO API.


## -enum-fields




### -field SERVICE_TYPE_IAS

The service is Internet Authentication Service (IAS) or Network Policy Server (NPS).

<div class="alert"><b>Note</b>  Internet Authentication Service was renamed Network Policy Server starting with Windows Server 2008.</div>
<div> </div>

### -field SERVICE_TYPE_RAS

The service is the Remote Access Service.


### -field SERVICE_TYPE_RAMGMTSVC

The service is the Remote Access Management Service.


### -field SERVICE_TYPE_MAX

Use this constant to test whether the value is in range.


## -see-also




<a href="https://msdn.microsoft.com/265f034a-78be-4792-958e-80ad7a71d1a7">ISdoMachine::GetServiceSDO</a>
 

 

