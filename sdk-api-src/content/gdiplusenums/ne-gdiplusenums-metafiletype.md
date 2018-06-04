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

# MetafileType enumeration


## -description


The <b>MetafileType</b> enumeration specifies types of metafiles. The 
			<a href="https://msdn.microsoft.com/42acdd2c-b87d-455a-83c0-0630bd552c45">MetafileHeader::GetType</a> method returns an element of this enumeration.


## -enum-fields




### -field MetafileTypeInvalid

Specifies a metafile format that is not recognized in GDI+. 


### -field MetafileTypeWmf

Specifies a WMF file. Such a file contains only GDI records. 


### -field MetafileTypeWmfPlaceable

Specifies a WMF file that has a placeable metafile header in front of it. 


### -field MetafileTypeEmf

Specifies an EMF file. Such a file contains only GDI records. 


### -field MetafileTypeEmfPlusOnly

Specifies an EMF+ file. Such a file contains only GDI+ records and must be displayed by using GDI+. Displaying the records using GDI may cause unpredictable results. 


### -field MetafileTypeEmfPlusDual

Specifies an EMF+ Dual file. Such a file contains GDI+ records along with alternative GDI records and can be displayed by using either GDI or GDI+. Displaying the records using GDI may cause some quality degradation. 


## -see-also




<a href="https://msdn.microsoft.com/42acdd2c-b87d-455a-83c0-0630bd552c45">MetafileHeader::GetType</a>
 

 

