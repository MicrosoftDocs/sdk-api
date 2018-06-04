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

# EmfType enumeration


## -description


The <b>EmfType</b> enumeration specifies the nature of the records that are placed in an Enhanced Metafile (EMF) file. This enumeration is used by several constructors in the 
			<a href="https://msdn.microsoft.com/63b057de-9c4d-488e-ad07-ede52f9175a6">Metafile</a> class.


## -enum-fields




### -field EmfTypeEmfOnly

Specifies that all of the records in the metafile are EMF records, which can be displayed by GDI or GDI+. 


### -field EmfTypeEmfPlusOnly

Specifies that all of the records in the metafile are EMF+ records, which can be displayed by GDI+ but not by GDI. 


### -field EmfTypeEmfPlusDual

Specifies that all EMF+ records in the metafile are associated with an alternate EMF record. Metafiles of type EmfTypeEmfPlusDual can be displayed by GDI or by GDI+. 


## -see-also




<a href="https://msdn.microsoft.com/a9648287-65d9-47d8-b32b-33f74b4fcd07">Metafile Constructors</a>
 

 

