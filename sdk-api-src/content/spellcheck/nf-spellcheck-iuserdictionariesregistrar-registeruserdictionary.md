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

# IUserDictionariesRegistrar::RegisterUserDictionary


## -description


Registers a file to be used as a user dictionary for the current user, until unregistered.


## -parameters




### -param dictionaryPath [in]

The path of the dictionary file to be registered.


### -param languageTag [in]

The language for which this dictionary should be used. If left empty, it will be used for any language.


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
<dt>S_FALSE</dt>
</dl>
</td>
<td width="60%">
The file is already registered for the language.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_INVALIDARG</dt>
</dl>
</td>
<td width="60%">
The file doesn’t exist or isn't valid, or it doesn't have a valid extension (.dic, .exc, or .acl)

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



The filename must have the extension .dic (added words), .exc (excluded words), or .acl (autocorrect word pairs). The files are  UTF-16 LE plaintext that must start with the appropriate Byte Order Mark (BOM). 
Each line contains a word (in the Added and Excluded word lists), or an autocorrect pair with the words separated by a vertical bar ("|") (in the AutoCorrect word list). The wordlist in which the dictionary is included is inferred through the file extension.

A file registered for a language subtag will be picked up for all languages that contain it. For example, a dictionary registered for "en" will also be used by an "en-US" spell checker.




## -see-also




<a href="https://msdn.microsoft.com/eca9446a-268e-4318-a5e7-8bb8592c9660">IUserDictionariesRegistrar</a>
 

 

