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

# IUserDictionariesRegistrar::UnregisterUserDictionary


## -description


Unregisters a previously registered user dictionary. The dictionary will no longer be used by the spell checking functionality.


## -parameters




### -param dictionaryPath [in]

The path of the dictionary file to be unregistered.


### -param languageTag [in]

The language for which this dictionary was used. It must match the language passed to <a href="https://msdn.microsoft.com/5dd64e20-af2d-4d84-9e66-01ac19f34212">RegisterUserDictionary</a>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
Successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_POINTER</dt>
</dl>
</td>
<td width="60%">
<i>dictionaryPath</i> or <i>languageTag</i> is a null pointer.

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  To unregister a given file, this method must be passed the same arguments that were previously used to register it.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/eca9446a-268e-4318-a5e7-8bb8592c9660">IUserDictionariesRegistrar</a>
 

 

