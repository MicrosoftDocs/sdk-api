---
UID: NF:spellcheckprovider.IComprehensiveSpellCheckProvider.ComprehensiveCheck
title: IComprehensiveSpellCheckProvider::ComprehensiveCheck (spellcheckprovider.h)
author: windows-sdk-content
description: Spell-check the provider text in a more thorough manner than ISpellCheckProvider::Check.
old-location: intl\icomprehensivespellcheckprovider_comprehensivecheck.htm
tech.root: Intl
ms.assetid: BD334EB8-4E14-478D-AB2A-E7F863C4BE0F
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ComprehensiveCheck, ComprehensiveCheck method [Internationalization for Windows Applications], ComprehensiveCheck method [Internationalization for Windows Applications],IComprehensiveSpellCheckProvider interface, IComprehensiveSpellCheckProvider interface [Internationalization for Windows Applications],ComprehensiveCheck method, IComprehensiveSpellCheckProvider.ComprehensiveCheck, IComprehensiveSpellCheckProvider::ComprehensiveCheck, intl.icomprehensivespellcheckprovider_comprehensivecheck, spellcheckprovider/IComprehensiveSpellCheckProvider::ComprehensiveCheck
ms.topic: method
req.header: spellcheckprovider.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - spellcheckprovider.h
api_name:
 - IComprehensiveSpellCheckProvider.ComprehensiveCheck
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComprehensiveSpellCheckProvider::ComprehensiveCheck


## -description


Spell-check the provider text in a more thorough manner than <a href="https://msdn.microsoft.com/B8C62B56-FF72-4C94-AC77-A6BEFCFE2589">ISpellCheckProvider::Check</a>.


## -parameters




### -param text [in]

The text to check.


### -param value [out]

The result of checking this text, as an enumeration of spelling errors (<a href="https://msdn.microsoft.com/bd284569-cafe-4993-a832-0683212c8b92">IEnumSpellingError</a>), if any.


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
<dt>E_INVALIDARG</dt>
</dl>
</td>
<td width="60%">
<i>text</i> is an empty string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_POINTER</dt>
</dl>
</td>
<td width="60%">
<i>text</i> is a null pointer.

</td>
</tr>
</table>
 




## -remarks



This interface isn't required to be implemented by a spell check provider. But if the provider supports two "modes" of spell checking (a faster one and a slower but more thorough one), it should implement this interface in the same object that implements <a href="https://msdn.microsoft.com/D7C8831E-6FCE-45E0-B2EB-4EB2B1F7911F">ISpellCheckProvider</a> to support the more thorough checking mode. 
When a client calls <a href="https://msdn.microsoft.com/E364F423-AF17-4F91-993B-CEA0E50CAF67">ISpellChecker::ComprehensiveCheck</a>, the spell checking functionality will <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> the provider for <a href="https://msdn.microsoft.com/303EE887-DCF0-4575-A45F-5A4088DE8F7B">IComprehensiveSpellCheckProvider</a>, and call <b>IComprehensiveSpellCheckProvider.ComprehensiveCheck</b> if the interface is supported. If the interface isn't supported, it will silently fall back to <a href="https://msdn.microsoft.com/B8C62B56-FF72-4C94-AC77-A6BEFCFE2589">ISpellCheckProvider::Check</a>.




## -see-also




<a href="https://msdn.microsoft.com/303EE887-DCF0-4575-A45F-5A4088DE8F7B">IComprehensiveSpellCheckProvider</a>



<a href="https://msdn.microsoft.com/bd284569-cafe-4993-a832-0683212c8b92">IEnumSpellingError</a>



<a href="https://msdn.microsoft.com/D7C8831E-6FCE-45E0-B2EB-4EB2B1F7911F">ISpellCheckProvider</a>



<a href="https://msdn.microsoft.com/B8C62B56-FF72-4C94-AC77-A6BEFCFE2589">ISpellCheckProvider::Check</a>



<a href="https://msdn.microsoft.com/E364F423-AF17-4F91-993B-CEA0E50CAF67">ISpellChecker::ComprehensiveCheck</a>
 

 

