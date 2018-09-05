---
UID: NS:rectypes.tagRECO_LATTICE
title: tagRECO_LATTICE
author: windows-sdk-content
description: Serves as the entry point into a lattice.
old-location: tablet\reco_lattice.htm
old-project: tablet
ms.assetid: 0fab8928-1632-4011-9d1d-2be5f6c5f22d
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: 0fab8928-1632-4011-9d1d-2be5f6c5f22d, RECO_LATTICE, RECO_LATTICE structure [Tablet PC], rectypes/RECO_LATTICE, tablet.reco_lattice, tagRECO_LATTICE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: rectypes.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: RECO_LATTICE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - rectypes.h
api_name:
 - RECO_LATTICE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# tagRECO_LATTICE structure


## -description



Serves as the entry point into a lattice.




## -struct-fields




### -field ulColumnCount

The number of columns in the lattice.


### -field pLatticeColumns

An array of <a href="https://msdn.microsoft.com/5695cae1-2bbf-48d4-a044-b2bd81c362d0">RECO_LATTICE_COLUMN</a> structures contained by the lattice.


### -field ulPropertyCount

The number of properties assigned to the lattice. For details about properties, see the <a href="https://msdn.microsoft.com/1c3501a9-398d-4db1-82b2-82908e132a4a">RECO_LATTICE_PROPERTIES</a> structure.


### -field pGuidProperties

An array of property GUIDs. The GUIDS for these properties can either be the properties defined in the Msinkaut.h header file (for example, line metrics) or custom properties defined by your recognizer.


### -field ulBestResultColumnCount

The number of columns that the best result consists of.


### -field pulBestResultColumns

An array containing the indexes of the columns in the <i>pLatticeColumns</i> array that makes up the best result.


### -field pulBestResultIndexes

An array of indexes of the elements in the <i>pLatticeElements</i> array of the corresponding column designated by <i>pulBestResultColumn</i>.


## -remarks



The <i>ulBestResultColumnCount</i>, <i>pulBestResultColumns</i>, and <i>pulBestResultIndexes</i> members are used together to hold information about the top alternates among all columns. These values should be filled in by the recognizer, even in the simplest case where there is no segmentation and there is only one column. Using the "together" <a href="https://msdn.microsoft.com/628ca677-31eb-47d9-bcc6-d7777f8aaf7c">example</a>, if the recognizer determines that the best result is "to gather", <i>ulBestResultColumnCount</i> would be 3, the <i>pulBestResultColumns</i> array would contain [0,1,2] and the <i>pulBestResultIndexes</i>  array would contain [1,0,2].




## -see-also




<a href="https://msdn.microsoft.com/5c483500-c58f-4fd0-903a-a3011727bab8">GetLatticePtr Function</a>



<a href="https://msdn.microsoft.com/5695cae1-2bbf-48d4-a044-b2bd81c362d0">RECO_LATTICE_COLUMN Structure</a>



<a href="https://msdn.microsoft.com/1c3501a9-398d-4db1-82b2-82908e132a4a">RECO_LATTICE_PROPERTIES Structure</a>



<a href="https://msdn.microsoft.com/628ca677-31eb-47d9-bcc6-d7777f8aaf7c">Recognizer Lattice Structure</a>
 

 

