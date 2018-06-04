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

# _IASDATASTORE enumeration


## -description


The values of the 
<b>IASDATASTORE</b> enumeration indicate the possible storage locations for SDO data.


## -enum-fields




### -field DATA_STORE_LOCAL

The SDO data is stored locally on the SDO computer.


### -field DATA_STORE_DIRECTORY

The SDO data is stored in the Active Directory.


## -remarks



You cannot use this enumeration type to specify the storage location for SDO data.




## -see-also




<a href="https://msdn.microsoft.com/265f034a-78be-4792-958e-80ad7a71d1a7">ISdoMachine::GetServiceSDO</a>



<a href="https://msdn.microsoft.com/c416c0db-836a-4056-bcd7-819f10923446">ISdoMachine::GetUserSDO</a>
 

 

