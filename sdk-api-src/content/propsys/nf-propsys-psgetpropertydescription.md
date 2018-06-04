---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# PSGetPropertyDescription function


## -description


Gets an instance of a property description interface for a property specified by a <a href="shell.PROPERTYKEY">PROPERTYKEY</a> structure.


## -parameters




### -param propkey [in]

Type: <b>REFPROPERTYKEY</b>

Reference to a <a href="shell.PROPERTYKEY">PROPERTYKEY</a>.


### -param riid [in]

Type: <b>REFIID</b>

Reference to the interface ID of the requested interface.


### -param ppv [out]

Type: <b>void**</b>

When this function returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="shell.IPropertyDescription">IPropertyDescription</a>, <a href="shell.IPropertyDescriptionAliasInfo">IPropertyDescriptionAliasInfo</a>, or <a href="shell.IPropertyDescriptionSearchInfo">IPropertyDescriptionSearchInfo</a>.


## -returns



Type: <b>PSSTDAPI</b>

Returns one of the following values.

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
The interface was obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppv</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_ELEMENTNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The <a href="shell.PROPERTYKEY">PROPERTYKEY</a> does not exist in the schema subsystem cache.

</td>
</tr>
</table>
 




## -remarks



We recommend that you use the <b>IID_PPV_ARGS</b> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.PSGetPropertyDescription">PSGetPropertyDescription</a> to get the property description for the ratings property.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IPropertyDescription *pPropDesc;

HRESULT hr = PSGetPropertyDescription(PKEY_Ratings, IID_PPV_ARGS(&amp;pPropDesc));

if (SUCCEEDED(hr))
{
    // pPropDesc is now valid.
 
    pPropDesc-&gt;Release();
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.PSGetPropertyDescriptionByName">PSGetPropertyDescriptionByName</a>



<a href="shell.PSGetPropertySystem">PSGetPropertySystem</a>
 

 

