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

# _DOMAINTYPE enumeration


## -description


The values of the 
<b>IASDOMAINTYPE</b> enumeration type specify whether the SDO computer is part of a domain, and if so, what type of domain.


## -enum-fields




### -field DOMAIN_TYPE_NONE

The SDO computer is running in stand-alone mode.


### -field DOMAIN_TYPE_NT4

Not supported.


### -field DOMAIN_TYPE_NT5

The SDO computer is part of a Windows domain running in native mode.


### -field DOMAIN_TYPE_MIXED

The SDO computer is part of a Windows domain running in mixed mode.


## -see-also




<a href="https://msdn.microsoft.com/83a3d4cf-e0ab-467a-8c5a-b7372c76cca3">IASOSTYPE</a>



<a href="https://msdn.microsoft.com/9c22ec67-4a12-4487-bac5-8f0e666b8029">ISdoMachine::GetDomainType</a>
 

 

