---
UID: NF:tapi3if.ITAddressTranslation.get_Locations
title: ITAddressTranslation::get_Locations
author: windows-sdk-content
description: The get_Locations method creates a collection of currently available address locations. This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the EnumerateLocations method.
old-location: tapi3\itaddresstranslation_get_locations.htm
old-project: tapi
ms.assetid: b18f7cb1-fcec-41eb-ac57-bf2d47f958e0
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: ITAddressTranslation interface [TAPI 2.2],get_Locations method, ITAddressTranslation.get_Locations, ITAddressTranslation::get_Locations, _tapi3_itaddresstranslation_get_locations, get_Locations, get_Locations method [TAPI 2.2], get_Locations method [TAPI 2.2],ITAddressTranslation interface, tapi3.itaddresstranslation_get_locations, tapi3if/ITAddressTranslation::get_Locations
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
 - ITAddressTranslation.get_Locations
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAddressTranslation::get_Locations


## -description


The 
<b>get_Locations</b> method creates a collection of currently available address locations. This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="https://msdn.microsoft.com/b286c738-1037-4a11-8c71-192b050d1502">EnumerateLocations</a> method.


## -parameters




### -param pVariant [out]

Pointer to <b>VARIANT</b> containing an 
<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a> of 
<a href="https://msdn.microsoft.com/0f82a6f4-26a6-48dc-9bfa-a86edf1b6be4">ITLocationInfo</a> interface pointers (location objects).


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
The <i>pVariant</i> parameter is not a valid pointer.

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



The 
<b>get_Locations</b> method is a COM wrapper for the TAPI 2.1 
<a href="https://msdn.microsoft.com/77437b06-fb02-44b5-8642-b3de700853ef">LineGetTranslateCaps</a> function, and takes location information from the 
<a href="https://msdn.microsoft.com/9b4dcbe6-41e9-4b9c-9150-d0c7edef5a19">LINETRANSLATECAPS</a> structure returned by that function.

TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/0f82a6f4-26a6-48dc-9bfa-a86edf1b6be4">ITLocationInfo</a> interface returned by <b>ITAddressTranslation::get_Locations</b>. The application must call <b>Release</b> on the 
<b>ITLocationInfo</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/b286c738-1037-4a11-8c71-192b050d1502">EnumerateLocations</a>



<a href="https://msdn.microsoft.com/e1cd88f1-1ed7-4e7f-a745-9a9c4af69317">ITAddressTranslation</a>



<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a>



<a href="https://msdn.microsoft.com/0f82a6f4-26a6-48dc-9bfa-a86edf1b6be4">ITLocationInfo</a>
 

 

