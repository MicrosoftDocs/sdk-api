---
UID: NS:rectypes.tagRECO_LATTICE_PROPERTY
title: RECO_LATTICE_PROPERTY (rectypes.h)
description: Contains a property used in the lattice.
helpviewer_keywords: ["RECO_LATTICE_PROPERTY","RECO_LATTICE_PROPERTY structure [Tablet PC]","cbf35f4e-cc13-4d5e-886f-22a6f0e26411","rectypes/RECO_LATTICE_PROPERTY","tablet.reco_lattice_property"]
old-location: tablet\reco_lattice_property.htm
tech.root: tablet
ms.assetid: cbf35f4e-cc13-4d5e-886f-22a6f0e26411
ms.date: 12/05/2018
ms.keywords: RECO_LATTICE_PROPERTY, RECO_LATTICE_PROPERTY structure [Tablet PC], cbf35f4e-cc13-4d5e-886f-22a6f0e26411, rectypes/RECO_LATTICE_PROPERTY, tablet.reco_lattice_property
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
req.typenames: RECO_LATTICE_PROPERTY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagRECO_LATTICE_PROPERTY
 - rectypes/tagRECO_LATTICE_PROPERTY
 - RECO_LATTICE_PROPERTY
 - rectypes/RECO_LATTICE_PROPERTY
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
 - RECO_LATTICE_PROPERTY
---

# RECO_LATTICE_PROPERTY structure


## -description

Contains a property used in the lattice.

## -struct-fields

### -field guidProperty

GUID for the property value that is being assigned.

### -field cbPropertyValue

Length in bytes of the <i>pPropertyValue</i> byte array.

### -field pPropertyValue

Byte array that points to the property data.

## -remarks

Properties can be stored on a column or an element. For example, the recognizer can store ink line break information about an alternate.

There are some predefined property GUIDs defined in the Msinkaut.h header file.

<table>
<tr>
<th>GUID</th>
<th>Description</th>
</tr>
<tr>
<td>
INKRECOGNITIONPROPERTY_CONFIDENCELEVEL

</td>
<td>
Describes whether the element contains wide string or wide character data.
<code>enum enumCONFIDENCE_LEVEL</code><code>{</code><code>CFL_STRONG = 0,</code><code>CFL_INTERMEDIATE = 1,</code><code>CFL_POOR = 2</code><code>} CONFIDENCE_LEVEL;</code></td>
</tr>
<tr>
<td>
INKRECOGNITIONPROPERTY_HOTPOINT

</td>
<td>
For gestures, identifies the part of the stroke that is the hot point. The hot point is the part of the stroke where the associated action is being applied.

</td>
</tr>
<tr>
<td>
INKRECOGNITIONPROPERTY_LINEMETRICS

</td>
<td>
Contains a <a href="/windows/desktop/api/rectypes/ns-rectypes-lattice_metrics">LATTICE_METRICS</a> structure that holds details about the baseline and midline for the element. To set this property, your recognizer must also set the INKRECOGNITIONPROPERTY_LINENUMBER property.

</td>
</tr>
<tr>
<td>
INKRECOGNITIONPROPERTY_LINENUMBER

</td>
<td>
A ULONG value containing the line that the element belongs to as determined by the recognizer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/rectypes/ns-rectypes-reco_lattice_column">RECO_LATTICE_COLUMN Structure</a>



<a href="/windows/desktop/api/rectypes/ns-rectypes-reco_lattice_element">RECO_LATTICE_ELEMENT Structure</a>



<a href="/windows/desktop/api/rectypes/ns-rectypes-reco_lattice_properties">RECO_LATTICE_PROPERTIES Structure</a>



<a href="/windows/desktop/tablet/recognizer-lattice-structure">Recognizer Lattice Structure</a>