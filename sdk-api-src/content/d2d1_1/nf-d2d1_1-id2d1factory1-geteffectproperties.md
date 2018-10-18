---
UID: NF:d2d1_1.ID2D1Factory1.GetEffectProperties
title: ID2D1Factory1::GetEffectProperties
author: windows-sdk-content
description: Retrieves the properties of an effect.
old-location: direct2d\id2d1factory1_geteffectproperties.htm
tech.root: direct2d
ms.assetid: 0e8a2f03-f297-4d5a-8461-4ed7cd1bf02f
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: GetEffectProperties, GetEffectProperties method [Direct2D], GetEffectProperties method [Direct2D],ID2D1Factory1 interface, ID2D1Factory1 interface [Direct2D],GetEffectProperties method, ID2D1Factory1.GetEffectProperties, ID2D1Factory1::GetEffectProperties, d2d1_1/ID2D1Factory1::GetEffectProperties, direct2d.id2d1factory1_geteffectproperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Factory1.GetEffectProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Factory1::GetEffectProperties


## -description


Retrieves the properties of an effect.


## -parameters




### -param effectId [in]

Type: <b>REFCLSID</b>

The ID of the effect to retrieve properties from.


### -param properties [out]

Type: <b><a href="https://msdn.microsoft.com/c38bfcc0-c696-41cc-9531-7c8f15c0b512">ID2D1Properties</a>**</b>

When this method returns, contains the address of a pointer to the property interface that can be used to query the metadata of the effect.


## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>No error occurred.</td>
</tr>
<tr>
<td>D2DERR_EFFECT_IS_NOT_REGISTERED</td>
<td>The requested effect could not be found.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>Direct2D could not allocate sufficient memory to complete the call.</td>
</tr>
</table>
 




## -remarks



The returned effect properties will have all the mutable properties for the effect set to a default of <b>NULL</b>, or an  empty value. 

<ul>
<li>Value types will be zero-filled.</li>
<li>Blob and string types will be zero-length.</li>
<li>Array types will have length 1 and the element of the array will conform to the previous rules.</li>
</ul>
This method cannot be used to return the properties for any effect not visible to <a href="https://msdn.microsoft.com/dfe587f9-e92f-4367-a503-edd446a91cb8">ID2D1DeviceContext::CreateEffect</a>.




## -see-also




<a href="https://msdn.microsoft.com/8221c3b4-e331-403c-9406-ee8d3e103825">ID2D1Factory1</a>



<a href="https://msdn.microsoft.com/c3363411-908f-4b02-b77e-ca563094f9a5">ID2D1Factory1::GetRegisteredEffects</a>



<a href="https://msdn.microsoft.com/9988aad6-0487-4f48-a05c-1dfb944f6ce7">ID2D1Factory1::RegisterEffect</a>
 

 

