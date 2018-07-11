---
UID: NF:spellcheckprovider.ISpellCheckProvider.SetOptionValue
title: ISpellCheckProvider::SetOptionValue
author: windows-sdk-content
description: Sets the value associated with the given option.
old-location: intl\ispellcheckprovider_setoptionvalue.htm
old-project: Intl
ms.assetid: 635E6024-DD9F-403D-B05F-B719EFE78FC0
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: ISpellCheckProvider interface [Internationalization for Windows Applications],SetOptionValue method, ISpellCheckProvider.SetOptionValue, ISpellCheckProvider::SetOptionValue, SetOptionValue, SetOptionValue method [Internationalization for Windows Applications], SetOptionValue method [Internationalization for Windows Applications],ISpellCheckProvider interface, intl.ispellcheckprovider_setoptionvalue, spellcheckprovider/ISpellCheckProvider::SetOptionValue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: spellcheckprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
 - ISpellCheckProvider.SetOptionValue
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISpellCheckProvider::SetOptionValue


## -description


Sets the value associated with the given option.


## -parameters




### -param optionId [in]

The option identifier.


### -param value [in]

The value to associate with <i>optionId</i>.


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
 




## -remarks



This method is called by the system, which reads the option values that were set by the user in the control panel and sends them to the <a href="https://msdn.microsoft.com/D7C8831E-6FCE-45E0-B2EB-4EB2B1F7911F">ISpellCheckProvider</a>. If the option was not set, this method will not be called and the provider should initialize itself internally with the default value for the option.




## -see-also




<a href="https://msdn.microsoft.com/D7C8831E-6FCE-45E0-B2EB-4EB2B1F7911F">ISpellCheckProvider</a>
 

 

