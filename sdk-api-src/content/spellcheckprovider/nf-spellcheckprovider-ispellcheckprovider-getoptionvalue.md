---
UID: NF:spellcheckprovider.ISpellCheckProvider.GetOptionValue
title: ISpellCheckProvider::GetOptionValue
author: windows-sdk-content
description: Retrieves the value associated with the given option.
old-location: intl\ispellcheckprovider_getoptionvalue.htm
tech.root: Intl
ms.assetid: 4EE5DE54-DCA2-4DDC-BDE1-6417E4ADF4A2
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: GetOptionValue, GetOptionValue method [Internationalization for Windows Applications], GetOptionValue method [Internationalization for Windows Applications],ISpellCheckProvider interface, ISpellCheckProvider interface [Internationalization for Windows Applications],GetOptionValue method, ISpellCheckProvider.GetOptionValue, ISpellCheckProvider::GetOptionValue, intl.ispellcheckprovider_getoptionvalue, spellcheckprovider/ISpellCheckProvider::GetOptionValue
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
 - ISpellCheckProvider.GetOptionValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpellCheckProvider::GetOptionValue


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




<a href="https://msdn.microsoft.com/D7C8831E-6FCE-45E0-B2EB-4EB2B1F7911F">ISpellCheckProvider</a>
 

 

