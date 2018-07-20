---
UID: NS:rectypes.tagRECO_LATTICE_COLUMN
title: tagRECO_LATTICE_COLUMN
author: windows-sdk-content
description: Represents a column in the lattice.
old-location: tablet\reco_lattice_column.htm
old-project: tablet
ms.assetid: 5695cae1-2bbf-48d4-a044-b2bd81c362d0
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: 5695cae1-2bbf-48d4-a044-b2bd81c362d0, RECO_LATTICE_COLUMN, RECO_LATTICE_COLUMN structure [Tablet PC], rectypes/RECO_LATTICE_COLUMN, tablet.reco_lattice_column, tagRECO_LATTICE_COLUMN
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: RECO_LATTICE_COLUMN
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - rectypes.h
api_name:
 - RECO_LATTICE_COLUMN
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# tagRECO_LATTICE_COLUMN structure


## -description



Represents a column in the lattice.




## -struct-fields




### -field key

Unused. Should be set to 0 (zero).


### -field cpProp

 Holds the properties for the column.


### -field cStrokes

Count of strokes in the <i>pStrokes</i> array for the longest element in the column.


### -field pStrokes

 An array of stroke indices in the order in which they were fed to the recognizer. For example, imagine you have two strokes, stroke one containing the word "back" and stroke two containing the word "door". The column containing "back" will have a strokes array containing one ULONG {0}. The column for "door" will have a strokes array containing two ULONG items {1,2}.


### -field cLatticeElements

Number of members in <i>pLatticeElements</i>.


### -field pLatticeElements

Array of <a href="https://msdn.microsoft.com/c4100cb9-d666-4e74-ac12-7f242b3c60d4">RECO_LATTICE_ELEMENT</a> structures.


## -remarks



There is one column per recognition segment. Each column contains one or more elements. An element is usually a word or character that is a recognition alternate. Elements start with the same stroke index, but do not necessarily contain the same number of strokes (for example, see column 0 in the "together" <a href="https://msdn.microsoft.com/628ca677-31eb-47d9-bcc6-d7777f8aaf7c">example</a>). The structure also holds properties that are valid for the whole column.




## -see-also




<a href="https://msdn.microsoft.com/1db3dbef-41bf-4b00-8e6c-07c7c414e595">AddStroke Function</a>



<a href="https://msdn.microsoft.com/c4100cb9-d666-4e74-ac12-7f242b3c60d4">RECO_LATTICE_ELEMENT Structure</a>
 

 

