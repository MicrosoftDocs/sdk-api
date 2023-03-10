---
UID: NN:d2d1_1.ID2D1Properties
title: ID2D1Properties (d2d1_1.h)
description: Represents a set of run-time bindable and discoverable properties that allow a data-driven application to modify the state of a Direct2D effect.
helpviewer_keywords: ["ID2D1Properties","ID2D1Properties interface [Direct2D]","ID2D1Properties interface [Direct2D]","described","d2d1_1/ID2D1Properties","direct2d.id2d1properties"]
old-location: direct2d\id2d1properties.htm
tech.root: Direct2D
ms.assetid: c38bfcc0-c696-41cc-9531-7c8f15c0b512
ms.date: 12/05/2018
ms.keywords: ID2D1Properties, ID2D1Properties interface [Direct2D], ID2D1Properties interface [Direct2D],described, d2d1_1/ID2D1Properties, direct2d.id2d1properties
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
req.lib: 
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Properties
 - d2d1_1/ID2D1Properties
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
 - ID2D1Properties
---

# ID2D1Properties interface


## -description

Represents a set of run-time bindable and discoverable properties that allow a data-driven application to modify the state of a Direct2D effect.

## -inheritance

The <b>ID2D1Properties</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID2D1Properties</b> also has these types of members:

## -remarks

This interface supports access through either indices or property names. In addition to top-level properties, each property in an <b>ID2D1Properties</b> object may contain an <b>ID2D1Properties</b> object, which stores metadata describing the parent property. 

<h3><a id="Overview"></a><a id="overview"></a><a id="OVERVIEW"></a>Overview</h3>
The <b>ID2D1Properties</b> interface exposes a set of run-time bindable and discoverable properties that allow a data-driven application such as an effect graph authoring tool or an animation system to modify the state of a Direct2D effect.

The interface supports access through either indices or property names. In addition to top-level properties, each property in an <b>ID2D1Properties</b> may contain a sub-<b>ID2D1Properties</b> interface, which stores metadata describing its parent property. Sub-properties are accessed by requesting this sub-interface by property index, or by using a property name string separated by a dot (.).

The interface is intentionally designed to avoid dependencies on a run-time basis. All allocation is done by the caller of the API and <b>VARIANT</b> types are not used. The property interface generally is designed not to return failures where the application could trivially change their calling sequence in order to avoid the condition. For example, since the number of properties supported by the instance is returned by the <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1properties-getpropertycount">GetPropertyCount</a> method, other methods that take a property index do not return a failure, unless they also use the plug-in effect's property system.

The interface is primarily based upon an index-based access model, and it supports nested sub-properties within properties. Unlike a directory structure, the property itself has a value and a type and might optionally support sub-properties (directories are not files). These are normally metadata that describe the property, but, this is also used to specify arrays of objects. In order to simplify accessing sub-properties and to allow name-based access, two helper methods – [GetValueByName](./nf-d2d1_1-id2d1properties-getvaluebyname(pcwstr).md) – are defined. These use a "dotted" notation in order to allow sub-properties to be directly specified, for example:


```cpp
alphaMode = pEffect->GetValueByName<UINT32>(L"Inputs.0.AlphaMode");
```




Or:


```cpp
pEffect->SetValueByName<UINT32>(
		    L"Inputs.0.AlphaMode", 
		    DXGI_ALPHA_MODE_PREMULTIPLIED);
		
```




<h3><a id="Standard_Effect_Properties"></a><a id="standard_effect_properties"></a><a id="STANDARD_EFFECT_PROPERTIES"></a>Standard Effect Properties</h3>
<table>
<tr>
<th>Property name/index</th>
<th>Property type</th>
<th>Property description</th>
</tr>
<tr>
<td>CLSID / D2D1_PROPERTY_CLSID</td>
<td>D2D1_PROPERTY_TYPE_CLSID</td>
<td>The CLSID of the effect.</td>
</tr>
<tr>
<td>DisplayName / D2D1_PROPERTY_DISPLAYNAME</td>
<td>D2D1_PROPERTY_TYPE_STRING</td>
<td>A displayable, localized name for the effect.</td>
</tr>
<tr>
<td>Author / D2D1_PROPERTY_AUTHOR</td>
<td>D2D1_PROPERTY_TYPE_STRING</td>
<td>The author of the effect.</td>
</tr>
<tr>
<td>Category / D2D1_PROPERTY_CATEGORY</td>
<td>D2D1_PROPERTY_TYPE_STRING</td>
<td>The category of the effect. </td>
</tr>
<tr>
<td>Description / D2D1_PROPERTY_DESCRIPTION</td>
<td>D2D1_PROPERTY_TYPE_STRING</td>
<td>A description of the effect. </td>
</tr>
<tr>
<td>Inputs / D2D1_PROPERTY_INPUTS</td>
<td>D2D1_PROPERTY_TYPE_ARRAY
			<div class="alert"><b>Note</b>  Elements of this array are of type D2D1_PROPERTY_TYPE_STRING.</div>
<div> </div>
</td>
<td>An array of names for the effect’s inputs. Each element of the array is a localized string specifying the name of an input.</td>
</tr>
</table>
 

<h3><a id="Standard_Sub-Properties"></a><a id="standard_sub-properties"></a><a id="STANDARD_SUB-PROPERTIES"></a>Standard Sub-Properties</h3>
The following are standard sub-properties that can be used for meta-data access, and may be available on both system and custom properties. Please see the <a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_subproperty">D2D1_SUBPROPERTY</a> and <a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_property_type">D2D1_PROPERTY_TYPE</a> enumerations for more information.

<table>
<tr>
<th>Property name/index</th>
<th>Property type</th>
<th>Property description</th>
</tr>
<tr>
<td>DisplayName / D2D1_SUBPROPERTY_DISPLAYNAME</td>
<td>D2D1_PROPERTY_TYPE_STRING</td>
<td>
A displayable, localized name for the parent property.

This sub-property is present on all  top-level properties.

</td>
</tr>
<tr>
<td>IsReadOnly / D2D1_SUBPROPERTY_ISREADONLY</td>
<td>D2D1_PROPERTY_TYPE_BOOL</td>
<td>
A value indicating whether the parent property can be written to.

This sub-property is present on all  top-level properties.

</td>
</tr>
<tr>
<td>Default / D2D1_SUBPROPERTY_DEFAULT</td>
<td>Same as parent property.</td>
<td>
The default value for the property.

This sub-property is optionally present on all properties.

</td>
</tr>
<tr>
<td>Min / D2D1_SUBPROPERTY_MIN</td>
<td>Same as parent property.
		  	<div class="alert"><b>Note</b>  Applicable only to numeric-type properties.</div>
<div> </div>
</td>
<td>
The minimum value that the parent property supports being set to.

</td>
</tr>
<tr>
<td>Max / D2D1_SUBPROPERTY_MAX</td>
<td>Same as parent property.
				<div class="alert"><b>Note</b>  Applicable only to numeric-type properties.</div>
<div> </div>
</td>
<td>
The maximum value that the parent property supports being set to.

</td>
</tr>
<tr>
<td>Fields / D2D1_SUBPROPERTY_FIELDS</td>
<td>Array / D2D1_PROPERTY_TYPE_ARRAY
				<div class="alert"><b>Note</b>  Applicable only when the parent property is of type <b>Enum</b>.</div>
<div> </div>
</td>
<td>
The set of valid values that can be set to the parent property.

Each value in this array is a name/index pair. The indices can be set to the parent and the names are localized values designed for consumption by UI. See the following section for more details.

</td>
</tr>
</table>
 

<h3><a id="Array-Type_Sub-Properties"></a><a id="array-type_sub-properties"></a><a id="ARRAY-TYPE_SUB-PROPERTIES"></a>Array-Type Sub-Properties</h3>
See <a href="/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-gettype(u)">ID2D1Properties::GetType</a> and <a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_property_type">D2D1_PROPERTY_TYPE</a> for more information. If the property type is <b>D2D1_PROPERTY_TYPE_ARRAY</b>, the value of the property will be considered to be a <b>UINT</b> that has the count of array elements. The next sub-property will directly map the index to the requested property value. For example:


```cpp
Inputs: UINT32 – 2
		Inputs.0 : <Type> – First input
		Inputs.1 : <Type> – Second input
		
```


The above example makes use of the following sub-properties, which will appear on <b>ARRAY</b>-type properties. Note that the numbered properties are not system properties, and are in the normal (0x0 – 0x80000000) range.

<table>
<tr>
<th>Property name</th>
<th>Property index</th>
<th>Property description</th>
</tr>
<tr>
<td>Property.0</td>
<td>0</td>
<td>First element of the property array.</td>
</tr>
<tr>
<td>...</td>
<td>...</td>
<td>...</td>
</tr>
<tr>
<td>Property.N</td>
<td>N</td>
<td><i>N</i>th element of the property array.</td>
</tr>
</table>
 

The type of each sub-element will be whatever the type of the array is. In the example above, this was an array of strings.

<h3><a id="Enum-Type_Sub-Poperties"></a><a id="enum-type_sub-poperties"></a><a id="ENUM-TYPE_SUB-POPERTIES"></a>Enum-Type Sub-Properties</h3>
If the property has type <b>D2D1_PROPERTY_TYPE_ENUM</b> then the property will have the value of the corresponding enumeration. There will be a sub-array of fields that will conform to the general rules for array sub-properties and consist of the name/value pairs. For example:


```cpp
PixelFormat: ENUM – The pixel format value
		PixelFormat.Fields: UINT32 – The number of fields
		PixelFormat.Fields.0:String – The name of the first enum
		PixelFormat.Fields.0.Index: UINT32 – The value of the enumeration.
		
```


The above example makes use of the following sub-properties. Please see the <a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_subproperty">D2D1_SUBPROPERTY</a> and <a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_property_type">D2D1_PROPERTY_TYPE</a> enumerations for more information.

<table>
<tr>
<th>Property name</th>
<th>Property index</th>
<th>Property description</th>
</tr>
<tr>
<td>Property.Fields</td>
<td>D2D1_SUBPROPERTY_FIELDS</td>
<td>An array type property that gives information about each field in the enumeration.</td>
</tr>
<tr>
<td>Property.Fields.N</td>
<td>N</td>
<td>An array element that gives the name of the <i>N</i>th enumeration value.</td>
</tr>
<tr>
<td>Property.Fields.N.Index</td>
<td>D2D1_SUBPROPERTY_INDEX</td>
<td>The index which corresponds to the <i>N</i>th enumeration value.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect">ID2D1Effect</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
