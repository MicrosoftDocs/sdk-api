---
UID: NF:spellcheckprovider.ISpellCheckProvider.GetOptionDescription
title: ISpellCheckProvider::GetOptionDescription
author: windows-sdk-content
description: Retrieves the information (id, description, heading and labels) of a specific option.
old-location: intl\ispellcheckprovider_getoptiondescription.htm
tech.root: Intl
ms.assetid: 0F2ED4B7-AE71-4431-83FE-739F7D0D5CD2
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetOptionDescription, GetOptionDescription method [Internationalization for Windows Applications], GetOptionDescription method [Internationalization for Windows Applications],ISpellCheckProvider interface, ISpellCheckProvider interface [Internationalization for Windows Applications],GetOptionDescription method, ISpellCheckProvider.GetOptionDescription, ISpellCheckProvider::GetOptionDescription, intl.ispellcheckprovider_getoptiondescription, spellcheckprovider/ISpellCheckProvider::GetOptionDescription
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
 - ISpellCheckProvider.GetOptionDescription
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpellCheckProvider::GetOptionDescription


## -description


Retrieves the information (id, description, heading and labels) of a specific option.


## -parameters




### -param optionId [in]

Identifier of the option to be retrieved.


### -param value [out, retval]


<a href="https://msdn.microsoft.com/809d1a71-bb14-4516-9624-2f10fe19a5d9">IOptionDescription</a> interface that contains the information about <i>optionId</i>.


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




<a href="https://msdn.microsoft.com/809d1a71-bb14-4516-9624-2f10fe19a5d9">IOptionDescription</a>



<a href="https://msdn.microsoft.com/D7C8831E-6FCE-45E0-B2EB-4EB2B1F7911F">ISpellCheckProvider</a>
 

 

