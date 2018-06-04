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

# PSGetPropertyDescriptionListFromString function


## -description


Gets an instance of a property description list interface for a specified property list.


## -parameters




### -param pszPropList [in]

Type: <b>LPCWSTR</b>

Pointer to a null-terminated, Unicode string that identifies the property list. See <a href="shell.IPropertySystem_GetPropertyDescriptionListFromString">IPropertySystem::GetPropertyDescriptionListFromString</a> for more information about the format of this parameter.


### -param riid [in]

Type: <b>REFIID</b>

Reference to the interface ID of the requested interface.


### -param ppv [out]

Type: <b>void**</b>

When this function returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="shell.IPropertyDescriptionList">IPropertyDescriptionList</a>.


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
</table>
 




## -remarks



This function calls the property subsystem implementation of <a href="shell.IPropertySystem_GetPropertyDescriptionListFromString">IPropertySystem::GetPropertyDescriptionListFromString</a> to obtain a collection of properties provided as a semicolon-delimited property list string.

We recommend that you use the <b>IID_PPV_ARGS</b> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error.

For more information about property schemas, see <a href="shell.Building_Property_Handlers_Property_Schemas">Property Schemas</a>.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.PSGetPropertyDescriptionListFromString">PSGetPropertyDescriptionListFromString</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IPropertyDescriptionList *pList;

HRESULT hr = PSGetPropertyDescriptionListFromString(L"prop:System.Title;System.Size",
                                                    IID_PPV_ARGS(&amp;pList));
                                                    
if (SUCCEEDED(hr))
{
    // pList is now valid.
 
    pList-&gt;Release();
}</pre>
</td>
</tr>
</table></span></div>


