---
UID: NF:spellcheckprovider.ISpellCheckProvider.Check
title: ISpellCheckProvider::Check
author: windows-sdk-content
description: Checks the spelling of the supplied text and returns a collection of spelling errors.
old-location: intl\ispellcheckprovider_check.htm
tech.root: Intl
ms.assetid: B8C62B56-FF72-4C94-AC77-A6BEFCFE2589
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Check, Check method [Internationalization for Windows Applications], Check method [Internationalization for Windows Applications],ISpellCheckProvider interface, ISpellCheckProvider interface [Internationalization for Windows Applications],Check method, ISpellCheckProvider.Check, ISpellCheckProvider::Check, intl.ispellcheckprovider_check, spellcheckprovider/ISpellCheckProvider::Check
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: spellcheckprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Spellcheckprovider.idl
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
 - Spellcheckprovider.h
api_name:
 - ISpellCheckProvider.Check
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpellCheckProvider::Check


## -description


Checks the spelling of the supplied text and returns a collection of spelling errors.


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



The returned <a href="https://msdn.microsoft.com/bd284569-cafe-4993-a832-0683212c8b92">IEnumSpellingError</a> should contain the results of spell checking. A correct <i>text</i> should return an empty (not a null) enumeration.




## -see-also




<a href="https://msdn.microsoft.com/bd284569-cafe-4993-a832-0683212c8b92">IEnumSpellingError</a>



<a href="https://msdn.microsoft.com/D7C8831E-6FCE-45E0-B2EB-4EB2B1F7911F">ISpellCheckProvider</a>
 

 

