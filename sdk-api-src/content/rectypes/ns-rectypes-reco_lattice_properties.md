---
UID: NS:rectypes.tagRECO_LATTICE_PROPERTIES
title: RECO_LATTICE_PROPERTIES (rectypes.h)
author: windows-sdk-content
description: Contains an array of pointers to property structures.
old-location: tablet\reco_lattice_properties.htm
tech.root: tablet
ms.assetid: 1c3501a9-398d-4db1-82b2-82908e132a4a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 1c3501a9-398d-4db1-82b2-82908e132a4a, RECO_LATTICE_PROPERTIES, RECO_LATTICE_PROPERTIES structure [Tablet PC], rectypes/RECO_LATTICE_PROPERTIES, tablet.reco_lattice_properties
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - rectypes.h
api_name:
 - RECO_LATTICE_PROPERTIES
product: Windows
targetos: Windows
req.typenames: RECO_LATTICE_PROPERTIES
req.redist: 
ms.custom: 19H1
---

# RECO_LATTICE_PROPERTIES structure


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




<a href="https://docs.microsoft.com/windows/desktop/api/rectypes/ns-rectypes-tagreco_lattice_column">RECO_LATTICE_COLUMN Structure</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rectypes/ns-rectypes-tagreco_lattice_element">RECO_LATTICE_ELEMENT Structure</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rectypes/ns-rectypes-tagreco_lattice_property">RECO_LATTICE_PROPERTY Structure</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/recognizer-lattice-structure">Recognizer Lattice Structure</a>
 

 

