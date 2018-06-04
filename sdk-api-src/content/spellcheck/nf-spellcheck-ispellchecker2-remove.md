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

# ISpellChecker2::Remove


## -description


Removes a word that was previously added by <a href="https://msdn.microsoft.com/d600a57e-7191-4a82-8004-026a04ef94ed">ISpellChecker.Add</a>, or set by <a href="https://msdn.microsoft.com/e82dd7a3-3ec4-4ef4-a19f-ad44866bbb1c">ISpellChecker.Ignore</a> to be ignored.


## -parameters




### -param word [in]

The word to be removed from the list of added words, or from the list of ignored words. If the word is not present, nothing will be removed.


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
<dt><b>E_ INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>word</i> is an empty string, or its length is greater than <b>MAX_WORD_LENGTH</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>word</i> is a null pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3cc5f675-048d-4ef3-9b66-5f081ee17a18">ISpellChecker</a>



<a href="https://msdn.microsoft.com/d600a57e-7191-4a82-8004-026a04ef94ed">ISpellChecker.Add</a>



<a href="https://msdn.microsoft.com/e82dd7a3-3ec4-4ef4-a19f-ad44866bbb1c">ISpellChecker.Ignore</a>



<a href="https://msdn.microsoft.com/615C52CD-BD4D-4AC0-9732-6AB6BD7A930F">ISpellChecker2</a>
 

 

