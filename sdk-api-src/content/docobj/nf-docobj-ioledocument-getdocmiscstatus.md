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

# IOleDocument::GetDocMiscStatus


## -description


Retrieves status information about the document object.


## -parameters




### -param pdwStatus [out]

A pointer to the information on supported behaviors. Possible values are taken from the <a href="https://msdn.microsoft.com/e52e022e-dd82-42f0-a3dd-2730ad80613c">DOCMISC</a> enumeration.


## -returns



This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>pdwStatus</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method provides a way for containers to ascertain whether a document object supports multiple views, complex rectangles, opening in a pop-up window, or file read/write.

Values from this enumerator are also stored in the registry as the value of the DocObject key.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
By calling this method prior to activating a document object, containers can take whatever steps are necessary to support or otherwise accommodate the specified behaviors.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
This method must be completely implemented in any document object, even if the dereferenced value of <i>pdwStatus</i> is zero. E_NOTIMPL is not an acceptable return value. Normally, the returned <a href="https://msdn.microsoft.com/e52e022e-dd82-42f0-a3dd-2730ad80613c">DOCMISC</a> value should be hard-coded for performance.




## -see-also




<a href="https://msdn.microsoft.com/e52e022e-dd82-42f0-a3dd-2730ad80613c">DOCMISC</a>



<a href="https://msdn.microsoft.com/7a15d6ef-900c-4a0b-8b85-60dc66ca03a3">IOleDocument</a>
 

 

