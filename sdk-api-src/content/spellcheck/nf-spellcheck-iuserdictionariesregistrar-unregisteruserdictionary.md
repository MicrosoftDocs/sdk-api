---
UID: NF:spellcheck.IUserDictionariesRegistrar.UnregisterUserDictionary
title: IUserDictionariesRegistrar::UnregisterUserDictionary
author: windows-sdk-content
description: Unregisters a previously registered user dictionary.
old-location: intl\iuserdictionariesregistrar_unregisteruserdictionary.htm
tech.root: Intl
ms.assetid: 6b1756f5-7ab5-4408-896d-5ea5ae671651
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: IUserDictionariesRegistrar interface [Internationalization for Windows Applications],UnregisterUserDictionary method, IUserDictionariesRegistrar.UnregisterUserDictionary, IUserDictionariesRegistrar::UnregisterUserDictionary, UnregisterUserDictionary, UnregisterUserDictionary method [Internationalization for Windows Applications], UnregisterUserDictionary method [Internationalization for Windows Applications],IUserDictionariesRegistrar interface, intl.iuserdictionariesregistrar_unregisteruserdictionary, spellcheck/IUserDictionariesRegistrar::UnregisterUserDictionary
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: spellcheck.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Spellcheck.idl
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
 - COM
api_location:
 - Spellcheck.h
api_name:
 - IUserDictionariesRegistrar.UnregisterUserDictionary
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

