---
UID: NF:spellcheckprovider.ISpellCheckProvider.Suggest
title: ISpellCheckProvider::Suggest
author: windows-sdk-content
description: Retrieves spelling suggestions for the supplied text.
old-location: intl\ispellcheckprovider_suggest.htm
tech.root: Intl
ms.assetid: 4A66619C-8A12-4465-889C-B880C43031AB
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISpellCheckProvider interface [Internationalization for Windows Applications],Suggest method, ISpellCheckProvider.Suggest, ISpellCheckProvider::Suggest, Suggest, Suggest method [Internationalization for Windows Applications], Suggest method [Internationalization for Windows Applications],ISpellCheckProvider interface, intl.ispellcheckprovider_suggest, spellcheckprovider/ISpellCheckProvider::Suggest
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
 - ISpellCheckProvider.Suggest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpellCheckProvider::Suggest


## -description


Retrieves spelling suggestions for the supplied text.


## -parameters




### -param word [in]

The word or phrase to get suggestions for.


### -param value [out, retval]

The list of suggestions, returned as an <a href="https://msdn.microsoft.com/7f3e642a-17c7-4646-8c70-da6b0946a415">IEnumString</a> object.


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
<i>word</i> is correctly spelled. <i>value</i> contains one entry, which is the text that was passed in.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>word</i> is an empty string.

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




<a href="https://msdn.microsoft.com/7f3e642a-17c7-4646-8c70-da6b0946a415">IEnumString</a>



<a href="https://msdn.microsoft.com/D7C8831E-6FCE-45E0-B2EB-4EB2B1F7911F">ISpellCheckProvider</a>
 

 

