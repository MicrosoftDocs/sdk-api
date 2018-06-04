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

# D3D12_SO_DECLARATION_ENTRY structure


## -description


Describes a vertex element in a vertex buffer in an output slot.


## -struct-fields




### -field Stream

Zero-based, stream number.


### -field SemanticName

Type of output element; possible values include: <b>"POSITION"</b>, <b>"NORMAL"</b>, or <b>"TEXCOORD0"</b>.
        Note that if <b>SemanticName</b> is <b>NULL</b> then 
        <b>ComponentCount</b> can be greater than 4 and the described entry will be a gap in the stream out where no data will be written.
        


### -field SemanticIndex

Output element's zero-based index. Use, for example, if you have more than one texture coordinate stored in each vertex.


### -field StartComponent

The component of the entry to begin writing out to. Valid values are 0 to 3. For example, if you only wish to output to the y and z components 
        of a position, <b>StartComponent</b> is 1 and <b>ComponentCount</b> is 2.


### -field ComponentCount

The number of components of the entry to write out to. Valid values are 1 to 4. For example, if you only wish to output to the y and z components 
        of a position, <b>StartComponent</b> is 1 and <b>ComponentCount</b> is 2.  Note that if <b>SemanticName</b> is <b>NULL</b> then 
        <b>ComponentCount</b> can be greater than 4 and the described entry will be a gap in the stream out where no data will be written.


### -field OutputSlot

The associated stream output buffer that is bound to the pipeline. 
        The valid range for <b>OutputSlot</b> is 0 to 3.


## -remarks



Specify an array of <b>D3D12_SO_DECLARATION_ENTRY</b> structures in the <b>pSODeclaration</b> member of a <a href="https://msdn.microsoft.com/9EFAA901-857B-40E3-B4B7-7C04D53BCA67">D3D12_STREAM_OUTPUT_DESC</a> structure. 




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

