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
 

 

