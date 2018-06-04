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

# IEnumSpellingError::Next


## -description


Gets the next spelling error.


## -parameters




### -param value [out, retval]

The spelling error (<a href="https://msdn.microsoft.com/90a233a4-44a4-4f8f-92bb-ea65fa213616">ISpellingError</a>) returned.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
There is no spelling error left to return.  <i>value</i> does not point at a valid <a href="https://msdn.microsoft.com/90a233a4-44a4-4f8f-92bb-ea65fa213616">ISpellingError</a>.

</td>
</tr>
</table>
 




## -remarks



If there are no spelling errors, this will return <b>S_FALSE</b>.
This provides a way for a provider to implement spell checking lazily if desired—instead of doing the spell checking work on <a href="https://msdn.microsoft.com/687d7e2f-13b1-4871-8850-2b179a6ce786">ISpellCheckProvider::Check</a> and getting all the errors at once, you can do it only as needed when this method is called, getting one error per call.




## -see-also




<a href="https://msdn.microsoft.com/bd284569-cafe-4993-a832-0683212c8b92">IEnumSpellingError</a>



<a href="https://msdn.microsoft.com/90a233a4-44a4-4f8f-92bb-ea65fa213616">ISpellingError</a>
 

 

