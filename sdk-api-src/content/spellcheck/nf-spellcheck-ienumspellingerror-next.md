---
UID: NF:spellcheck.IEnumSpellingError.Next
title: IEnumSpellingError::Next method
author: windows-driver-content
description: Gets the next spelling error.
old-location: intl\ienumspellingerror_next.htm
old-project: Intl
ms.assetid: c0fba585-2511-4162-8232-4e0510dc9261
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IEnumSpellingError, IEnumSpellingError interface [Internationalization for Windows Applications], Next method, IEnumSpellingError::Next, Next method [Internationalization for Windows Applications], Next method [Internationalization for Windows Applications], IEnumSpellingError interface, Next,IEnumSpellingError.Next, intl.ienumspellingerror_next, spellcheck/IEnumSpellingError::Next
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: spellcheck.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Spellcheck.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WORDLIST_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Spellcheck.h
api_name:
-	IEnumSpellingError.Next
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IEnumSpellingError::Next method


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
 

 

