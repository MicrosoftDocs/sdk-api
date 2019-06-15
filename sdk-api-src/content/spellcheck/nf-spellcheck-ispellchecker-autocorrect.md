---
UID: NF:spellcheck.ISpellChecker.AutoCorrect
title: ISpellChecker::AutoCorrect (spellcheck.h)
author: windows-sdk-content
description: Causes occurrences of one word to be replaced by another.
old-location: intl\ispellchecker_autocorrect.htm
tech.root: Intl
ms.assetid: 7c0d24dc-cec2-4304-bfbc-096fa4d0e8d0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AutoCorrect, AutoCorrect method [Internationalization for Windows Applications], AutoCorrect method [Internationalization for Windows Applications],ISpellChecker interface, ISpellChecker interface [Internationalization for Windows Applications],AutoCorrect method, ISpellChecker.AutoCorrect, ISpellChecker::AutoCorrect, intl.ispellchecker_autocorrect, spellcheck/ISpellChecker::AutoCorrect
ms.topic: method
f1_keywords: ["spellcheck/ISpellChecker.AutoCorrect"]
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
 - ISpellChecker.AutoCorrect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISpellChecker::AutoCorrect


## -description


Causes occurrences of one word to be replaced by another.


## -parameters




### -param from [in]

The incorrectly spelled word to be autocorrected.


### -param to [in]

The correctly spelled word that should replace <i>from</i>.


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
<i>from</i> or <i>to</i> is an empty string, or the length of at least one of the parameters is greater than <b>MAX_WORD_LENGTH</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>from</i> or <i>to</i> is a null pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/spellcheck/nn-spellcheck-ispellchecker">ISpellChecker</a>
 

 

