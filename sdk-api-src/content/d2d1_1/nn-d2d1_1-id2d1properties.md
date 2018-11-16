---
UID: NN:d2d1_1.ID2D1Properties
title: ID2D1Properties
author: windows-sdk-content
description: Represents a set of run-time bindable and discoverable properties that allow a data-driven application to modify the state of a Direct2D effect.
old-location: direct2d\id2d1properties.htm
tech.root: Direct2D
ms.assetid: c38bfcc0-c696-41cc-9531-7c8f15c0b512
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ID2D1Properties, ID2D1Properties interface [Direct2D], ID2D1Properties interface [Direct2D],described, d2d1_1/ID2D1Properties, direct2d.id2d1properties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Properties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Properties interface


## -description


Represents a set of run-time bindable and discoverable properties that allow a data-driven application to modify the state of a Direct2D effect.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1Properties</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID2D1Properties</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1Properties</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/abf54fef-8b46-41f9-a87e-c9c58e8ee49e">GetPropertyCount</a>
</td>
<td align="left" width="63%">
Gets the number of top-level properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b1c7003f-b7c2-464c-8e8e-a641068b9393">GetPropertyIndex</a>
</td>
<td align="left" width="63%">
Gets the index corresponding to the given property name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9FE7EA1D-18BB-47A6-9E73-14A6820F7D9D">GetPropertyName overload methods</a>
</td>
<td align="left" width="63%">
Gets the property name that corresponds to the given index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EA0B4C07-AD15-42C3-9300-26E51E310420">GetPropertyNameLength overload methods</a>
</td>
<td align="left" width="63%">
Gets  the number of characters for the given property name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AC1DA115-F6D4-47AB-8440-C4BD21E64A86">GetSubProperties overload methods</a>
</td>
<td align="left" width="63%">
Gets the sub-properties of the provided property by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BD4A7C13-83E2-4403-AEFC-B4718D67FEBB">GetType overload methods</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/6535d71a-c76c-462c-9972-4db7e4ef383d">D2D1_PROPERTY_TYPE</a> of the selected property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27535422-C213-4595-915E-445F72416C5E">GetValue overload methods</a>
</td>
<td align="left" width="63%">
Gets  the value of the property by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55904A81-3BF8-4A86-8A85-52D1BF6C19B7">GetValueByName overload methods</a>
</td>
<td align="left" width="63%">
Gets the property value by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62D47611-1AF7-45F3-BB7B-20BF478811BE">GetValueSize overload methods</a>
</td>
<td align="left" width="63%">
Gets the size of the property value in bytes, using the property index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FA740482-BAAF-466F-8CD1-330253B581BF">SetValue overload methods</a>
</td>
<td align="left" width="63%">
Sets the corresponding property by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E00C7BDA-B950-435E-AFD8-216FB0E3BA8C">SetValueByName overload methods</a>
</td>
<td align="left" width="63%">
Sets the named property to the given value.

</td>
</tr>
</table> 


## -remarks



This interface supports access through either indices or property names. In addition to top-level properties, each property in an <b>ID2D1Properties</b> object may contain an <b>ID2D1Properties</b> object, which stores metadata describing the parent property. 

<h3><a id="Overview"></a><a id="overview"></a><a id="OVERVIEW"></a>Overview</h3>
The <b>ID2D1Properties</b> interface exposes a set of run-time bindable and discoverable properties that allow a data-driven application such as an effect graph authoring tool or an animation system to modify the state of a Direct2D effect.

The interface supports access through either indices or property names. In addition to top-level properties, each property in an <b>ID2D1Properties</b> may contain a sub-<b>ID2D1Properties</b> interface, which stores metadata describing its parent property. Sub-properties are accessed by requesting this sub-interface by property index, or by using a property name string separated by a dot (.).

The interface is intentionally designed to avoid dependencies on a run-time basis. All allocation is done by the caller of the API and <b>VARIANT</b> types are not used. The property interface generally is designed not to return failures where the application could trivially change their calling sequence in order to avoid the condition. For example, since the number of properties supported by the instance is returned by the <a href="https://msdn.microsoft.com/abf54fef-8b46-41f9-a87e-c9c58e8ee49e">GetPropertyCount</a> method, other methods that take a property index do not return a failure, unless they also use the plug-in effect's property system.

The interface is primarily based upon an index-based access model, and it supports nested sub-properties within properties. Unlike a directory structure, the property itself has a value and a type and might optionally support sub-properties (directories are not files). These are normally metadata that describe the property, but, this is also used to specify arrays of objects. In order to simplify accessing sub-properties and to allow name-based access, two helper methods – <a href="https://msdn.microsoft.com/3faedf5e-9329-4502-a1c9-162fd7b00319">SetValueByName</a> and <a href="https://msdn.microsoft.com/2dc60fad-9ce2-4951-85ea-647a828420a1">GetValueByName</a> – are defined. These use a "dotted" notation in order to allow sub-properties to be directly specified, for example:<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>alphaMode = pEffect-&gt;GetValueByName&lt;UINT32&gt;(L"Inputs.0.AlphaMode");</pre>
</td>
</tr>
</table></span></div>


Or:<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>pEffect-&gt;SetValueByName&lt;UINT32&gt;(
		    L"Inputs.0.AlphaMode", 
		    DXGI_ALPHA_MODE_PREMULTIPLIED);
		</pre>
</td>
</tr>
</table></span></div>


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
The following are standard sub-properties that can be used for meta-data access, and may be available on both system and custom properties. Please see the <a href="https://msdn.microsoft.com/311a1b6f-ef0e-4453-a5fe-d06ebb0bb222">D2D1_SUBPROPERTY</a> and <a href="https://msdn.microsoft.com/6535d71a-c76c-462c-9972-4db7e4ef383d">D2D1_PROPERTY_TYPE</a> enumerations for more information.

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
<td>Max / D2D1_SUBPROPERTY_MIN</td>
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
See <a href="https://msdn.microsoft.com/42e80588-9e80-4f30-9a3c-77b64f88ff7a">ID2D1Properties::GetType</a> and <a href="https://msdn.microsoft.com/6535d71a-c76c-462c-9972-4db7e4ef383d">D2D1_PROPERTY_TYPE</a> for more information. If the property type is <b>D2D1_PROPERTY_TYPE_ARRAY</b>, the value of the property will be considered to be a <b>UINT</b> that has the count of array elements. The next sub-property will directly map the index to the requested property value. For example:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>Inputs: UINT32 – 2
		Inputs.0 : &lt;Type&gt; – First input
		Inputs.1 : &lt;Type&gt; – Second input
		</pre>
</td>
</tr>
</table></span></div>
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

<h3><a id="Enum-Type_Sub-Poperties"></a><a id="enum-type_sub-poperties"></a><a id="ENUM-TYPE_SUB-POPERTIES"></a>Enum-Type Sub-Poperties</h3>
If the property has type <b>D2D1_PROPERTY_TYPE_ENUM</b> then the property will have the value of the corresponding enumeration. There will be a sub-array of fields that will conform to the general rules for array sub-properties and consist of the name/value pairs. For example:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>PixelFormat: ENUM – The pixel format value
		PixelFormat.Fields: UINT32 – The number of fields
		PixelFormat.Fields.0:String – The name of the first enum
		PixelFormat.Fields.0.Index: UINT32 – The value of the enumeration.
		</pre>
</td>
</tr>
</table></span></div>
The above example makes use of the following sub-properties. Please see the <a href="https://msdn.microsoft.com/311a1b6f-ef0e-4453-a5fe-d06ebb0bb222">D2D1_SUBPROPERTY</a> and <a href="https://msdn.microsoft.com/6535d71a-c76c-462c-9972-4db7e4ef383d">D2D1_PROPERTY_TYPE</a> enumerations for more information.

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




<a href="https://msdn.microsoft.com/e90d1830-c356-48f1-ac7b-1d94c8c26569">ID2D1Effect</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

