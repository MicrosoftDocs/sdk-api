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

# tagRECO_LATTICE_PROPERTIES structure


## -description



Contains an array of pointers to property structures.




## -struct-fields




### -field cProperties

A count of the properties in the array of properties.


### -field apProps

An array of pointers to properties.


## -remarks



The <i>apProps</i> element contains an array of pointers to properties rather than the structures themselves so that property values can be reused with multiple elements with lower memory usage.




## -see-also




<a href="https://msdn.microsoft.com/5695cae1-2bbf-48d4-a044-b2bd81c362d0">RECO_LATTICE_COLUMN Structure</a>



<a href="https://msdn.microsoft.com/c4100cb9-d666-4e74-ac12-7f242b3c60d4">RECO_LATTICE_ELEMENT Structure</a>



<a href="https://msdn.microsoft.com/cbf35f4e-cc13-4d5e-886f-22a6f0e26411">RECO_LATTICE_PROPERTY Structure</a>



<a href="https://msdn.microsoft.com/628ca677-31eb-47d9-bcc6-d7777f8aaf7c">Recognizer Lattice Structure</a>
 

 

