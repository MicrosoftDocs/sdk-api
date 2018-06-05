---
UID: NS:rectypes.tagRECO_LATTICE_ELEMENT
title: tagRECO_LATTICE_ELEMENT
author: windows-sdk-content
description: Corresponds to one word or one East Asian character, typically; however, an element may also correspond to a gesture, a shape, or some other code.
old-location: tablet\reco_lattice_element.htm
old-project: tablet
ms.assetid: c4100cb9-d666-4e74-ac12-7f242b3c60d4
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: RECO_LATTICE_ELEMENT, RECO_LATTICE_ELEMENT structure [Tablet PC], c4100cb9-d666-4e74-ac12-7f242b3c60d4, rectypes/RECO_LATTICE_ELEMENT, tablet.reco_lattice_element, tagRECO_LATTICE_ELEMENT
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
req.typenames: RECO_LATTICE_ELEMENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	rectypes.h
api_name:
-	RECO_LATTICE_ELEMENT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# tagRECO_LATTICE_ELEMENT structure


## -description



Corresponds to one word or one East Asian character, typically; however, an element may also correspond to a gesture, a shape, or some other code.




## -struct-fields




### -field score

Integer value that represents the shape probability assigned for this element.


### -field type

Describes whether the element contains wide string or wide character data.

<code>enum enumRECO_TYPE</code><code>{</code><code>RECO_TYPE_WSTRING = 0,</code><code>RECO_TYPE_WCHAR = 1</code><code>} RECO_TYPE;</code>


### -field pData

Holds the recognition result. This can be a string or a character.

Note: For recognizers of Latin script, the <code>pData</code> member contains a pointer to a <b>NULL</b>–terminated string of wide characters. For recognizers of East Asian characters, the <code>pData</code> member contains the wide character (WCHAR) value itself.


### -field ulNextColumn

Contains the index for the next column.


### -field ulStrokeNumber

Count of strokes used by this alternate.


### -field epProp

Properties structure. These are properties that are applicable to this element only.

For details about properties, see the <a href="https://msdn.microsoft.com/1c3501a9-398d-4db1-82b2-82908e132a4a">RECO_LATTICE_PROPERTIES</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/1c3501a9-398d-4db1-82b2-82908e132a4a">RECO_LATTICE_PROPERTIES Structure</a>



<a href="https://msdn.microsoft.com/628ca677-31eb-47d9-bcc6-d7777f8aaf7c">Recognizer Lattice Structure</a>
 

 

