---
UID: NF:spellcheck.ISpellChecker.ComprehensiveCheck
title: ISpellChecker::ComprehensiveCheck (spellcheck.h)
author: windows-sdk-content
description: Checks the spelling of the supplied text in a more thorough manner than ISpellChecker::Check, and returns a collection of spelling errors.
old-location: intl\ispellchecker_comprehensivecheck.htm
tech.root: Intl
ms.assetid: E364F423-AF17-4F91-993B-CEA0E50CAF67
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ComprehensiveCheck, ComprehensiveCheck method [Internationalization for Windows Applications], ComprehensiveCheck method [Internationalization for Windows Applications],ISpellChecker interface, ISpellChecker interface [Internationalization for Windows Applications],ComprehensiveCheck method, ISpellChecker.ComprehensiveCheck, ISpellChecker::ComprehensiveCheck, intl.ispellchecker_comprehensivecheck, spellcheck/ISpellChecker::ComprehensiveCheck
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
 - ISpellChecker.ComprehensiveCheck
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpellChecker::ComprehensiveCheck


## -description


Checks the spelling of the supplied text in a more thorough manner than <a href="https://msdn.microsoft.com/687d7e2f-13b1-4871-8850-2b179a6ce786">ISpellChecker::Check</a>, and returns a collection of spelling errors.


## -parameters




### -param text [in]

The text to check.


### -param value [out, retval]

The result of checking this text, returned as an <a href="https://msdn.microsoft.com/bd284569-cafe-4993-a832-0683212c8b92">IEnumSpellingError</a> object.


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
<i>text</i> is an empty string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>text</i> is a null pointer.

</td>
</tr>
</table>
 




## -remarks



The returned <a href="https://msdn.microsoft.com/bd284569-cafe-4993-a832-0683212c8b92">IEnumSpellingError</a> contains the results of spell checking. A correct <i>text</i> returns an empty (not a null) enumeration.

If the provider supports two "modes" of spell checking (a faster one and a slower but more thorough one), it implements <a href="https://msdn.microsoft.com/303EE887-DCF0-4575-A45F-5A4088DE8F7B">IComprehensiveSpellCheckProvider</a> to support the more thorough checking mode. 
When a client calls <b>ISpellChecker::ComprehensiveCheck</b>, the spell checking functionality will <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> the provider for <b>IComprehensiveSpellCheckProvider</b>, and call <a href="https://msdn.microsoft.com/BD334EB8-4E14-478D-AB2A-E7F863C4BE0F">IComprehensiveSpellCheckProvider.ComprehensiveCheck</a> if the interface is supported. If the interface isn't supported, it will silently fall back to <a href="https://msdn.microsoft.com/B8C62B56-FF72-4C94-AC77-A6BEFCFE2589">ISpellCheckProvider::Check</a>.




## -see-also




<a href="https://msdn.microsoft.com/303EE887-DCF0-4575-A45F-5A4088DE8F7B">IComprehensiveSpellCheckProvider</a>



<a href="https://msdn.microsoft.com/BD334EB8-4E14-478D-AB2A-E7F863C4BE0F">IComprehensiveSpellCheckProvider.ComprehensiveCheck</a>



<a href="https://msdn.microsoft.com/bd284569-cafe-4993-a832-0683212c8b92">IEnumSpellingError</a>



<a href="https://msdn.microsoft.com/D7C8831E-6FCE-45E0-B2EB-4EB2B1F7911F">ISpellCheckProvider</a>



<a href="https://msdn.microsoft.com/B8C62B56-FF72-4C94-AC77-A6BEFCFE2589">ISpellCheckProvider::Check</a>



<a href="https://msdn.microsoft.com/3cc5f675-048d-4ef3-9b66-5f081ee17a18">ISpellChecker</a>
 

 

