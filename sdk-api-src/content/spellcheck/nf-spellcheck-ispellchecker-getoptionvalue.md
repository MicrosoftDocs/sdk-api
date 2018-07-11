---
UID: NF:spellcheck.ISpellChecker.GetOptionValue
title: ISpellChecker::GetOptionValue
author: windows-sdk-content
description: Retrieves the value associated with the given option.
old-location: intl\ispellchecker_getoptionvalue.htm
old-project: Intl
ms.assetid: bdbf4fa6-9827-40d5-81c0-008e166c9390
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: GetOptionValue, GetOptionValue method [Internationalization for Windows Applications], GetOptionValue method [Internationalization for Windows Applications],ISpellChecker interface, ISpellChecker interface [Internationalization for Windows Applications],GetOptionValue method, ISpellChecker.GetOptionValue, ISpellChecker::GetOptionValue, intl.ispellchecker_getoptionvalue, spellcheck/ISpellChecker::GetOptionValue
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WORDLIST_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Spellcheck.h
api_name:
 - ISpellChecker.GetOptionValue
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISpellChecker::GetOptionValue


## -description


Retrieves the value associated with the given option.


## -parameters




### -param optionId [in]

The option identifier.


### -param value [out, retval]

The value associated with <i>optionId</i>.


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
<i>optionId</i> is an empty string, or it is not one of the available options.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>optionId</i> is a null pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3cc5f675-048d-4ef3-9b66-5f081ee17a18">ISpellChecker</a>
 

 

