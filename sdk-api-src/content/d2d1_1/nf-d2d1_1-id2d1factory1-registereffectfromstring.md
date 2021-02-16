---
UID: NF:d2d1_1.ID2D1Factory1.RegisterEffectFromString
title: ID2D1Factory1::RegisterEffectFromString (d2d1_1.h)
description: Registers an effect within the factory instance with the property XML specified as a string.
helpviewer_keywords: ["ID2D1Factory1 interface [Direct2D]","RegisterEffectFromString method","ID2D1Factory1.RegisterEffectFromString","ID2D1Factory1::RegisterEffectFromString","RegisterEffectFromString","RegisterEffectFromString method [Direct2D]","RegisterEffectFromString method [Direct2D]","ID2D1Factory1 interface","d2d1_1/ID2D1Factory1::RegisterEffectFromString","direct2d.id2d1factory1_registereffect"]
old-location: direct2d\id2d1factory1_registereffect.htm
tech.root: Direct2D
ms.assetid: 9988aad6-0487-4f48-a05c-1dfb944f6ce7
ms.date: 12/05/2018
ms.keywords: ID2D1Factory1 interface [Direct2D],RegisterEffectFromString method, ID2D1Factory1.RegisterEffectFromString, ID2D1Factory1::RegisterEffectFromString, RegisterEffectFromString, RegisterEffectFromString method [Direct2D], RegisterEffectFromString method [Direct2D],ID2D1Factory1 interface, d2d1_1/ID2D1Factory1::RegisterEffectFromString, direct2d.id2d1factory1_registereffect
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Factory1::RegisterEffectFromString
 - d2d1_1/ID2D1Factory1::RegisterEffectFromString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Factory1.RegisterEffectFromString
---

# ID2D1Factory1::RegisterEffectFromString


## -description

Registers an effect within the factory instance with the property XML specified as a string.

## -parameters

### -param classId [in]

Type: <b>REFCLSID</b>

The identifier of the effect to be registered.

### -param propertyXml [in]

Type: <b><a href="/windows/desktop/api/chstring/nf-chstring-chstring-chstring(lpcwstr)">PCWSTR</a></b>

A list of the effect properties, types, and metadata.

### -param bindings [in, optional]

Type: <b>const <a href="/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding">D2D1_PROPERTY_BINDING</a>*</b>

An array of properties and methods.

This binds a property by name to a particular method implemented by the effect author to handle the property. 
              The name must be found in the corresponding <i>propertyXml</i>.

### -param bindingsCount

Type: <b><a href="/windows/desktop/api/webservices/ns-webservices-ws_uint32_description">UINT32</a></b>

The number of bindings in the binding array.

### -param effectFactory

Type: <b><a href="/windows/desktop/api/d2d1_1/nc-d2d1_1-pd2d1_effect_factory">PD2D1_EFFECT_FACTORY</a></b>

The static factory that is used to create the corresponding effect.

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
        and can also declare custom properties. See <a href="/windows/desktop/Direct2D/custom-effects">Custom effects</a> 
        for more information about formatting the <i>propertyXml</i> parameter.
      

<b>RegisterEffect</b> is both atomic and reference counted. To unregister an effect, 
        call <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1factory1-unregistereffect">UnregisterEffect</a> with the  <i>classId</i> of the effect.
      

<div class="alert"><b>Important</b>  <b>RegisterEffect</b> does not hold a reference to the DLL or executable file in which 
          the effect is contained. The application must independently  make sure that the lifetime of the DLL or executable file completely contains all instances of each registered and created effect.
        </div>
<div> </div>
Aside from the <a href="/windows/desktop/Direct2D/built-in-effects">built-in effects</a> that are globally registered, this API registers effects only for 
      this factory and derived device and device context interfaces.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1">ID2D1Factory1</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1factory1-unregistereffect">ID2D1Factory1::UnregisterEffect</a>