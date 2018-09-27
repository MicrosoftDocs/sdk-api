---
UID: NF:spellcheck.ISpellChecker.Ignore
title: ISpellChecker::Ignore
author: windows-sdk-content
description: Ignores the provided word for the rest of this session.
old-location: intl\ispellchecker_ignore.htm
tech.root: Intl
ms.assetid: e82dd7a3-3ec4-4ef4-a19f-ad44866bbb1c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ISpellChecker interface [Internationalization for Windows Applications],Ignore method, ISpellChecker.Ignore, ISpellChecker::Ignore, Ignore, Ignore method [Internationalization for Windows Applications], Ignore method [Internationalization for Windows Applications],ISpellChecker interface, intl.ispellchecker_ignore, spellcheck/ISpellChecker::Ignore
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
 - ISpellChecker.Ignore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpellChecker::Ignore


## -description


Ignores the provided word for the rest of this session.

Until this <a href="https://msdn.microsoft.com/3cc5f675-048d-4ef3-9b66-5f081ee17a18">ISpellChecker</a> interface is released, the word  will no longer be considered misspelled, but it will not be considered as a candidate for suggestions.


## -parameters




### -param word [in]

The word to ignore.


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
 

 

