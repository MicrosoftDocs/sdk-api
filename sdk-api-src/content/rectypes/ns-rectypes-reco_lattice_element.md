---
UID: NS:rectypes.tagRECO_LATTICE_ELEMENT
title: RECO_LATTICE_ELEMENT (rectypes.h)
description: Corresponds to one word or one East Asian character, typically; however, an element may also correspond to a gesture, a shape, or some other code.
helpviewer_keywords: ["RECO_LATTICE_ELEMENT","RECO_LATTICE_ELEMENT structure [Tablet PC]","c4100cb9-d666-4e74-ac12-7f242b3c60d4","rectypes/RECO_LATTICE_ELEMENT","tablet.reco_lattice_element"]
old-location: tablet\reco_lattice_element.htm
tech.root: tablet
ms.assetid: c4100cb9-d666-4e74-ac12-7f242b3c60d4
ms.date: 12/05/2018
ms.keywords: RECO_LATTICE_ELEMENT, RECO_LATTICE_ELEMENT structure [Tablet PC], c4100cb9-d666-4e74-ac12-7f242b3c60d4, rectypes/RECO_LATTICE_ELEMENT, tablet.reco_lattice_element
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
req.typenames: RECO_LATTICE_ELEMENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagRECO_LATTICE_ELEMENT
 - rectypes/tagRECO_LATTICE_ELEMENT
 - RECO_LATTICE_ELEMENT
 - rectypes/RECO_LATTICE_ELEMENT
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
 - RECO_LATTICE_ELEMENT
---

# RECO_LATTICE_ELEMENT structure


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

For details about properties, see the <a href="/windows/desktop/api/rectypes/ns-rectypes-reco_lattice_properties">RECO_LATTICE_PROPERTIES</a> structure.

## -see-also

<a href="/windows/desktop/api/rectypes/ns-rectypes-reco_lattice_properties">RECO_LATTICE_PROPERTIES Structure</a>



<a href="/windows/desktop/tablet/recognizer-lattice-structure">Recognizer Lattice Structure</a>