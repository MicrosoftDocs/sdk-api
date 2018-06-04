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
 

 

