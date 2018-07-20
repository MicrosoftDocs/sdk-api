---
UID: NF:tapi3if.ITAddressTranslation.EnumerateCallingCards
title: ITAddressTranslation::EnumerateCallingCards
author: windows-sdk-content
description: The EnumerateCallingCards method enumerates calling cards associated with the address. This method is provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the get_CallingCards method.
old-location: tapi3\itaddresstranslation_enumeratecallingcards.htm
old-project: tapi
ms.assetid: 93f3cea1-70da-41f0-a8d5-692468a21695
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: EnumerateCallingCards, EnumerateCallingCards method [TAPI 2.2], EnumerateCallingCards method [TAPI 2.2],ITAddressTranslation interface, ITAddressTranslation interface [TAPI 2.2],EnumerateCallingCards method, ITAddressTranslation.EnumerateCallingCards, ITAddressTranslation::EnumerateCallingCards, _tapi3_itaddresstranslation_enumeratecallingcards, tapi3.itaddresstranslation_enumeratecallingcards, tapi3if/ITAddressTranslation::EnumerateCallingCards
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAddressTranslation.EnumerateCallingCards
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAddressTranslation::EnumerateCallingCards


## -description


The 
<b>EnumerateCallingCards</b> method enumerates calling cards associated with the address. This method is provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the 
<a href="https://msdn.microsoft.com/3033c584-1a7b-4bba-a8a2-2a2d59247689">get_CallingCards</a> method.


## -parameters




### -param ppEnumCallingCard [out]

Pointer to 
<a href="https://msdn.microsoft.com/d2eed88b-9a01-4205-a35d-92a24e07a1e2">IEnumCallingCard</a> interface.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppEnumCallingCard</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>
 




## -remarks



This method is a COM wrapper for the TAPI 2.1 
<a href="https://msdn.microsoft.com/77437b06-fb02-44b5-8642-b3de700853ef">LineGetTranslateCaps</a> function, and takes calling card information from the 
<a href="https://msdn.microsoft.com/9b4dcbe6-41e9-4b9c-9150-d0c7edef5a19">LINETRANSLATECAPS</a> structure returned by that function.

TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/d2eed88b-9a01-4205-a35d-92a24e07a1e2">IEnumCallingCard</a> interface returned by <b>ITAddressTranslation::EnumerateCallingCards</b>. The application must call <b>Release</b> on the 
<b>IEnumCallingCard</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/d2eed88b-9a01-4205-a35d-92a24e07a1e2">IEnumCallingCard</a>



<a href="https://msdn.microsoft.com/e1cd88f1-1ed7-4e7f-a745-9a9c4af69317">ITAddressTranslation</a>
 

 

