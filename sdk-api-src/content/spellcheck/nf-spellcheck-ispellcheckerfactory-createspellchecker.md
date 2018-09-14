---
UID: NF:spellcheck.ISpellCheckerFactory.CreateSpellChecker
title: ISpellCheckerFactory::CreateSpellChecker
author: windows-sdk-content
description: Creates a spell checker that supports the specified language.
old-location: intl\ispellcheckerfactory_createspellchecker.htm
tech.root: Intl
ms.assetid: 9167b675-01ec-4173-a790-5452907b5598
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: CreateSpellChecker, CreateSpellChecker method [Internationalization for Windows Applications], CreateSpellChecker method [Internationalization for Windows Applications],ISpellCheckerFactory interface, ISpellCheckerFactory interface [Internationalization for Windows Applications],CreateSpellChecker method, ISpellCheckerFactory.CreateSpellChecker, ISpellCheckerFactory::CreateSpellChecker, intl.ispellcheckerfactory_createspellchecker, spellcheck/ISpellCheckerFactory::CreateSpellChecker
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
 - ISpellCheckerFactory.CreateSpellChecker
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpellCheckerFactory::CreateSpellChecker


## -description


Creates a spell checker that supports the specified language.


## -parameters




### -param languageTag [in]

A <a href="http://go.microsoft.com/fwlink/p/?linkid=227302">BCP47</a> language tag that identifies the language for the requested spell checker.


### -param value [out, retval]

The created spell checker.


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
<i>languageTag</i> is an empty string, or there is no spell checker available for <i>languageTag</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>languageTag</i> is a null pointer.

</td>
</tr>
</table>
 




## -remarks




<a href="https://msdn.microsoft.com/eb21850d-d490-4055-8910-70f9c0090f59">ISpellCheckerFactory::IsSupported</a> can be called to determine if <i>languageTag</i> is supported.
This will create the preferred spell checker (according to user ranking) for the given language.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=227302">BCP47 Tags for Identifying Languages</a>



<a href="https://msdn.microsoft.com/3cc5f675-048d-4ef3-9b66-5f081ee17a18">ISpellChecker</a>



<a href="https://msdn.microsoft.com/7febbb7e-c557-4698-bf58-6e6e7f61b071">ISpellCheckerFactory</a>



<a href="https://msdn.microsoft.com/eb21850d-d490-4055-8910-70f9c0090f59">ISpellCheckerFactory::IsSupported</a>
 

 

