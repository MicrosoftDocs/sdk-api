---
UID: NS:rectypes.tagRECO_LATTICE
title: RECO_LATTICE (rectypes.h)
description: Serves as the entry point into a lattice.
helpviewer_keywords: ["0fab8928-1632-4011-9d1d-2be5f6c5f22d","RECO_LATTICE","RECO_LATTICE structure [Tablet PC]","rectypes/RECO_LATTICE","tablet.reco_lattice"]
old-location: tablet\reco_lattice.htm
tech.root: tablet
ms.assetid: 0fab8928-1632-4011-9d1d-2be5f6c5f22d
ms.date: 12/05/2018
ms.keywords: 0fab8928-1632-4011-9d1d-2be5f6c5f22d, RECO_LATTICE, RECO_LATTICE structure [Tablet PC], rectypes/RECO_LATTICE, tablet.reco_lattice
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RECO_LATTICE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagRECO_LATTICE
 - rectypes/tagRECO_LATTICE
 - RECO_LATTICE
 - rectypes/RECO_LATTICE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - rectypes.h
api_name:
 - RECO_LATTICE
---

# RECO_LATTICE structure


## -description

Serves as the entry point into a lattice.

## -struct-fields

### -field ulColumnCount

The number of columns in the lattice.

### -field pLatticeColumns

An array of <a href="/windows/desktop/api/rectypes/ns-rectypes-reco_lattice_column">RECO_LATTICE_COLUMN</a> structures contained by the lattice.

### -field ulPropertyCount

The number of properties assigned to the lattice. For details about properties, see the <a href="/windows/desktop/api/rectypes/ns-rectypes-reco_lattice_properties">RECO_LATTICE_PROPERTIES</a> structure.

### -field pGuidProperties

An array of property GUIDs. The GUIDS for these properties can either be the properties defined in the Msinkaut.h header file (for example, line metrics) or custom properties defined by your recognizer.

### -field ulBestResultColumnCount

The number of columns that the best result consists of.

### -field pulBestResultColumns

An array containing the indexes of the columns in the <i>pLatticeColumns</i> array that makes up the best result.

### -field pulBestResultIndexes

An array of indexes of the elements in the <i>pLatticeElements</i> array of the corresponding column designated by <i>pulBestResultColumn</i>.

## -remarks

The <i>ulBestResultColumnCount</i>, <i>pulBestResultColumns</i>, and <i>pulBestResultIndexes</i> members are used together to hold information about the top alternates among all columns. These values should be filled in by the recognizer, even in the simplest case where there is no segmentation and there is only one column. Using the "together" <a href="/windows/desktop/tablet/recognizer-lattice-structure">example</a>, if the recognizer determines that the best result is "to gather", <i>ulBestResultColumnCount</i> would be 3, the <i>pulBestResultColumns</i> array would contain [0,1,2] and the <i>pulBestResultIndexes</i>  array would contain [1,0,2].

## -see-also

<a href="/windows/desktop/api/recapis/nf-recapis-getlatticeptr">GetLatticePtr Function</a>



<a href="/windows/desktop/api/rectypes/ns-rectypes-reco_lattice_column">RECO_LATTICE_COLUMN Structure</a>



<a href="/windows/desktop/api/rectypes/ns-rectypes-reco_lattice_properties">RECO_LATTICE_PROPERTIES Structure</a>



<a href="/windows/desktop/tablet/recognizer-lattice-structure">Recognizer Lattice Structure</a>