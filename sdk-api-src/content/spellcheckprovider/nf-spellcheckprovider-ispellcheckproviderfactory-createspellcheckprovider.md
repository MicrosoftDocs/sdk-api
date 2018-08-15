---
UID: NF:spellcheckprovider.ISpellCheckProviderFactory.CreateSpellCheckProvider
title: ISpellCheckProviderFactory::CreateSpellCheckProvider
author: windows-sdk-content
description: Creates a spell checker (implemented by a spell check provider) that supports the specified language.
old-location: intl\ispellcheckproviderfactory_createspellcheckprovider.htm
old-project: Intl
ms.assetid: E56E13D5-A41D-41F4-8E63-55664F6A8E28
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateSpellCheckProvider, CreateSpellCheckProvider method [Internationalization for Windows Applications], CreateSpellCheckProvider method [Internationalization for Windows Applications],ISpellCheckProviderFactory interface, ISpellCheckProviderFactory interface [Internationalization for Windows Applications],CreateSpellCheckProvider method, ISpellCheckProviderFactory.CreateSpellCheckProvider, ISpellCheckProviderFactory::CreateSpellCheckProvider, intl.ispellcheckproviderfactory_createspellcheckprovider, spellcheckprovider/ISpellCheckProviderFactory::CreateSpellCheckProvider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: spellcheckprovider.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WORDLIST_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Spellcheckprovider.h
api_name:
 - ISpellCheckProviderFactory.CreateSpellCheckProvider
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISpellCheckProviderFactory::CreateSpellCheckProvider


## -description


Creates a spell checker (implemented by a spell check provider) that supports the specified language. This interface is not used directly by clients, but by the Spell Checking API.


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




<a href="https://msdn.microsoft.com/88689384-E95E-4D56-BAD4-9889816F76EB">ISpellCheckProviderFactory::IsSupported</a> can be called to determine if <i>languageTag</i> is supported.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=227302">BCP47 Tags for Identifying Languages</a>



<a href="https://msdn.microsoft.com/D7C8831E-6FCE-45E0-B2EB-4EB2B1F7911F">ISpellCheckProvider</a>



<a href="https://msdn.microsoft.com/680EC2D1-740E-40A8-9721-AC53AF17AC09">ISpellCheckProviderFactory</a>



<a href="https://msdn.microsoft.com/88689384-E95E-4D56-BAD4-9889816F76EB">ISpellCheckProviderFactory::IsSupported</a>
 

 

