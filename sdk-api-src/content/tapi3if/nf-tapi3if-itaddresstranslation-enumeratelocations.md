---
UID: NF:tapi3if.ITAddressTranslation.EnumerateLocations
title: ITAddressTranslation::EnumerateLocations
author: windows-sdk-content
description: The EnumerateLocations method enumerates the currently available address locations. This method is provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the get_Locations method.
old-location: tapi3\itaddresstranslation_enumeratelocations.htm
tech.root: tapi
ms.assetid: b286c738-1037-4a11-8c71-192b050d1502
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: EnumerateLocations, EnumerateLocations method [TAPI 2.2], EnumerateLocations method [TAPI 2.2],ITAddressTranslation interface, ITAddressTranslation interface [TAPI 2.2],EnumerateLocations method, ITAddressTranslation.EnumerateLocations, ITAddressTranslation::EnumerateLocations, _tapi3_itaddresstranslation_enumeratelocations, tapi3.itaddresstranslation_enumeratelocations, tapi3if/ITAddressTranslation::EnumerateLocations
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAddressTranslation.EnumerateLocations
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tapi3if.h
: 
- ITAddressTranslation.EnumerateLocations
: 
---

# ITAddressTranslation::EnumerateLocations


## -description


The 
<b>EnumerateLocations</b> method enumerates the currently available address locations. This method is provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the 
<a href="https://msdn.microsoft.com/b18f7cb1-fcec-41eb-ac57-bf2d47f958e0">get_Locations</a> method.


## -parameters




### -param ppEnumLocation [out]

Pointer to 
<a href="https://msdn.microsoft.com/fc8c235c-92ec-448f-bbea-c93192d36beb">IEnumLocation</a> object created.


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
The <i>ppEnumLocations</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to create object.

</td>
</tr>
</table>
 




## -remarks



The 
<b>EnumerateLocations</b> method is a COM wrapper for the TAPI 2.1 
<a href="https://msdn.microsoft.com/77437b06-fb02-44b5-8642-b3de700853ef">LineGetTranslateCaps</a> function, and takes location information from the 
<a href="https://msdn.microsoft.com/9b4dcbe6-41e9-4b9c-9150-d0c7edef5a19">LINETRANSLATECAPS</a> structure returned by that function.

TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/fc8c235c-92ec-448f-bbea-c93192d36beb">IEnumLocation</a> interface returned by <b>ITAddressTranslation::EnumerateLocations</b>. The application must call <b>Release</b> on the 
<b>IEnumLocation</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/fc8c235c-92ec-448f-bbea-c93192d36beb">IEnumLocation</a>



<a href="https://msdn.microsoft.com/e1cd88f1-1ed7-4e7f-a745-9a9c4af69317">ITAddressTranslation</a>
 

 

