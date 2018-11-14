---
UID: NF:d2d1_1.ID2D1Factory1.RegisterEffectFromString
title: ID2D1Factory1::RegisterEffectFromString
author: windows-sdk-content
description: Registers an effect within the factory instance with the property XML specified as a string.
old-location: direct2d\id2d1factory1_registereffect.htm
tech.root: direct2d
ms.assetid: 9988aad6-0487-4f48-a05c-1dfb944f6ce7
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: ID2D1Factory1 interface [Direct2D],RegisterEffectFromString method, ID2D1Factory1.RegisterEffectFromString, ID2D1Factory1::RegisterEffectFromString, RegisterEffectFromString, RegisterEffectFromString method [Direct2D], RegisterEffectFromString method [Direct2D],ID2D1Factory1 interface, d2d1_1/ID2D1Factory1::RegisterEffectFromString, direct2d.id2d1factory1_registereffect
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
 - ID2D1Factory1.RegisterEffectFromString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d2d1_1.h
: 
- ID2D1Factory1.RegisterEffectFromString
: 
---

# ID2D1Factory1::RegisterEffectFromString


## -description


Registers an effect within the factory instance with the property XML specified as a string.


## -parameters




### -param classId [in]

Type: <b>REFCLSID</b>

The identifier of the effect to be registered.


### -param propertyXml [in]

Type: <b><a href="https://msdn.microsoft.com/11780ce1-b7d8-4a79-89fc-656ea5d71048">PCWSTR</a></b>

A list of the effect properties, types, and metadata.


### -param bindings

TBD


### -param bindingsCount

Type: <b><a href="https://msdn.microsoft.com/dcb864f2-f162-41ca-b3ef-5b592a311299">UINT32</a></b>

The number of bindings in the binding array.


### -param effectFactory

Type: <b><a href="https://msdn.microsoft.com/e4f99762-4328-4b9c-ab0d-14b78a1581b5">PD2D1_EFFECT_FACTORY</a></b>

The static factory that is used to create the corresponding effect.


#### - Bindings [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/0eb6d428-cb65-4738-9cf3-64038b728004">D2D1_PROPERTY_BINDING</a>*</b>

An array of properties and methods.

This binds a property by name to a particular method implemented by the effect author to handle the property. 
              The name must be found in the corresponding <i>propertyXml</i>.
            


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
<td>E_OUTOFMEMORY</td>
<td>Direct2D could not allocate sufficient memory to complete the call.
                </td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid parameter was passed to the returning function.</td>
</tr>
</table>
 




## -remarks



Direct2D effects must define their properties at registration time via registration XML. An effect declares several required system properties, 
        and can also declare custom properties. See <a href="https://msdn.microsoft.com/5D22CA84-6465-4882-863D-81A632ACDD9C">Custom effects</a> 
        for more information about formatting the <i>propertyXml</i> parameter.
      

<b>RegisterEffect</b> is both atomic and reference counted. To unregister an effect, 
        call <a href="https://msdn.microsoft.com/5f383406-5d83-4ccc-9082-526b9e9fa80b">UnregisterEffect</a> with the  <i>classId</i> of the effect.
      

<div class="alert"><b>Important</b>  <b>RegisterEffect</b> does not hold a reference to the DLL or executable file in which 
          the effect is contained. The application must independently  make sure that the lifetime of the DLL or executable file completely contains all instances of each registered and created effect.
        </div>
<div> </div>
Aside from the <a href="https://msdn.microsoft.com/A76F6AB8-16E9-45C9-A768-5E4AA072D534">built-in effects</a> that are globally registered, this API registers effects only for 
      this factory and derived device and device context interfaces.




## -see-also




<a href="https://msdn.microsoft.com/8221c3b4-e331-403c-9406-ee8d3e103825">ID2D1Factory1</a>



<a href="https://msdn.microsoft.com/5f383406-5d83-4ccc-9082-526b9e9fa80b">ID2D1Factory1::UnregisterEffect</a>
 

 

