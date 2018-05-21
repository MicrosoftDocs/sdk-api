---
UID: NS:rectypes.tagRECO_LATTICE_PROPERTIES
title: tagRECO_LATTICE_PROPERTIES
author: windows-driver-content
description: Contains an array of pointers to property structures.
old-location: tablet\reco_lattice_properties.htm
old-project: tablet
ms.assetid: 1c3501a9-398d-4db1-82b2-82908e132a4a
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: 1c3501a9-398d-4db1-82b2-82908e132a4a, RECO_LATTICE_PROPERTIES, RECO_LATTICE_PROPERTIES structure [Tablet PC], rectypes/RECO_LATTICE_PROPERTIES, tablet.reco_lattice_properties, tagRECO_LATTICE_PROPERTIES
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: rectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RECO_LATTICE_PROPERTIES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	rectypes.h
api_name:
-	RECO_LATTICE_PROPERTIES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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
 

 

