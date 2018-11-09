---
UID: NF:propsys.PSGetPropertyDescription
title: PSGetPropertyDescription function
author: windows-sdk-content
description: Gets an instance of a property description interface for a property specified by a PROPERTYKEY structure.
old-location: properties\PSGetPropertyDescription.htm
tech.root: properties
ms.assetid: 03d98a40-1bfb-4df3-bc8b-eee6c49014d7
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: PSGetPropertyDescription, PSGetPropertyDescription function [Windows Properties], properties.PSGetPropertyDescription, propsys/PSGetPropertyDescription, shell.PSGetPropertyDescription, shell_PSGetPropertyDescription
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PSGetPropertyDescription
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# PSGetPropertyDescription function


## -description


Gets an instance of a property description interface for a property specified by a <a href="https://msdn.microsoft.com/en-us/library/Bb773381(v=VS.85).aspx">PROPERTYKEY</a> structure.


## -parameters




### -param propkey [in]

Type: <b>REFPROPERTYKEY</b>

Reference to a <a href="https://msdn.microsoft.com/en-us/library/Bb773381(v=VS.85).aspx">PROPERTYKEY</a>.


### -param riid [in]

Type: <b>REFIID</b>

Reference to the interface ID of the requested interface.


### -param ppv [out]

Type: <b>void**</b>

When this function returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="https://msdn.microsoft.com/en-us/library/Bb761561(v=VS.85).aspx">IPropertyDescription</a>, <a href="https://msdn.microsoft.com/en-us/library/Bb761517(v=VS.85).aspx">IPropertyDescriptionAliasInfo</a>, or <a href="https://msdn.microsoft.com/en-us/library/Bb761505(v=VS.85).aspx">IPropertyDescriptionSearchInfo</a>.


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
The <a href="https://msdn.microsoft.com/en-us/library/Bb773381(v=VS.85).aspx">PROPERTYKEY</a> does not exist in the schema subsystem cache.

</td>
</tr>
</table>
 




## -remarks



We recommend that you use the <b>IID_PPV_ARGS</b> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/en-us/library/Bb776503(v=VS.85).aspx">PSGetPropertyDescription</a> to get the property description for the ratings property.

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




<a href="https://msdn.microsoft.com/en-us/library/Bb776504(v=VS.85).aspx">PSGetPropertyDescriptionByName</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb762082(v=VS.85).aspx">PSGetPropertySystem</a>
 

 

