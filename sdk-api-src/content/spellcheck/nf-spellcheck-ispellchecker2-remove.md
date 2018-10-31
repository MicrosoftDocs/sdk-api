---
UID: NF:spellcheck.ISpellChecker2.Remove
title: ISpellChecker2::Remove
author: windows-sdk-content
description: Removes a word that was previously added by ISpellChecker.Add, or set by ISpellChecker.Ignore to be ignored.
old-location: intl\ispellchecker2_remove.htm
tech.root: Intl
ms.assetid: 425F1C58-D279-48E2-84D3-D3094314C756
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ISpellChecker2 interface [Internationalization for Windows Applications],Remove method, ISpellChecker2.Remove, ISpellChecker2::Remove, Remove, Remove method [Internationalization for Windows Applications], Remove method [Internationalization for Windows Applications],ISpellChecker2 interface, intl.ispellchecker2_remove, spellcheck/ISpellChecker2::Remove
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: spellcheck.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - ISpellChecker2.Remove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

