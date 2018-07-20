---
UID: NF:tapi3if.ITLegacyCallMediaControl2.CreateCustomToneObject
title: ITLegacyCallMediaControl2::CreateCustomToneObject
author: windows-sdk-content
description: The CreateCustomToneObject method creates a custom tone object to use with the GenerateCustomTonesByCollection method.
old-location: tapi3\itlegacycallmediacontrol2_createcustomtoneobject.htm
old-project: tapi
ms.assetid: addef387-9d92-4da3-af4c-b4d40bde2e36
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: CreateCustomToneObject, CreateCustomToneObject method [TAPI 2.2], CreateCustomToneObject method [TAPI 2.2],ITLegacyCallMediaControl2 interface, ITLegacyCallMediaControl2 interface [TAPI 2.2],CreateCustomToneObject method, ITLegacyCallMediaControl2.CreateCustomToneObject, ITLegacyCallMediaControl2::CreateCustomToneObject, _tapi3_itlegacycallmediacontrol2_createcustomtoneobject, tapi3.itlegacycallmediacontrol2_createcustomtoneobject, tapi3if/ITLegacyCallMediaControl2::CreateCustomToneObject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: 
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
 - ITLegacyCallMediaControl2.CreateCustomToneObject
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITLegacyCallMediaControl2::CreateCustomToneObject


## -description


The 
<b>CreateCustomToneObject</b> method creates a custom tone object to use with the 
<a href="https://msdn.microsoft.com/5115192e-68de-4779-92dc-7cf63585faae">GenerateCustomTonesByCollection</a> method.

This method is intended for Visual Basic and scripting applications. C/C++ applications should use the 
<a href="https://msdn.microsoft.com/fcc5d3c9-a7ab-4467-a948-b9fd68afe7b4">GenerateCustomTones</a> method instead.


## -parameters




### -param ppCustomTone [out]

Pointer to an 
<a href="https://msdn.microsoft.com/f2c51048-93aa-4469-b00e-911e62b5702d">ITCustomTone</a> interface.


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
The <i>ppCustomTone</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to allocate the object.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/f2c51048-93aa-4469-b00e-911e62b5702d">ITCustomTone</a> interface returned by <b>ITLegacyCallMediaControl2::CreateCustomToneObject</b>. The application must call the <b>Release</b> method on the 
<b>ITCustomTone</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/5115192e-68de-4779-92dc-7cf63585faae">GenerateCustomTonesByCollection</a>



<a href="https://msdn.microsoft.com/f2c51048-93aa-4469-b00e-911e62b5702d">ITCustomTone</a>



<a href="https://msdn.microsoft.com/47fa5669-1c74-4c18-8370-3efe35b3573e">ITLegacyCallMediaControl2</a>
 

 

