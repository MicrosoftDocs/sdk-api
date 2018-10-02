---
UID: NS:rectypes.tagRECO_LATTICE_PROPERTY
title: tagRECO_LATTICE_PROPERTY
author: windows-sdk-content
description: Contains a property used in the lattice.
old-location: tablet\reco_lattice_property.htm
tech.root: tablet
ms.assetid: cbf35f4e-cc13-4d5e-886f-22a6f0e26411
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: RECO_LATTICE_PROPERTY, RECO_LATTICE_PROPERTY structure [Tablet PC], cbf35f4e-cc13-4d5e-886f-22a6f0e26411, rectypes/RECO_LATTICE_PROPERTY, tablet.reco_lattice_property, tagRECO_LATTICE_PROPERTY
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
 - RECO_LATTICE_PROPERTY
product: Windows
targetos: Windows
req.typenames: RECO_LATTICE_PROPERTY
req.redist: 
---

# tagRECO_LATTICE_PROPERTY structure


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
Contains a <a href="https://msdn.microsoft.com/4fdeaaf9-9026-4bf1-8e78-d03a98d44b32">LATTICE_METRICS</a> structure that holds details about the baseline and midline for the element. To set this property, your recognizer must also set the INKRECOGNITIONPROPERTY_LINENUMBER property.

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




<a href="https://msdn.microsoft.com/5695cae1-2bbf-48d4-a044-b2bd81c362d0">RECO_LATTICE_COLUMN Structure</a>



<a href="https://msdn.microsoft.com/c4100cb9-d666-4e74-ac12-7f242b3c60d4">RECO_LATTICE_ELEMENT Structure</a>



<a href="https://msdn.microsoft.com/1c3501a9-398d-4db1-82b2-82908e132a4a">RECO_LATTICE_PROPERTIES Structure</a>



<a href="https://msdn.microsoft.com/628ca677-31eb-47d9-bcc6-d7777f8aaf7c">Recognizer Lattice Structure</a>
 

 

