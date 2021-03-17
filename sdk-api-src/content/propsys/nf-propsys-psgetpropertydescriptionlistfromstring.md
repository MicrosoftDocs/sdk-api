---
UID: NF:propsys.PSGetPropertyDescriptionListFromString
title: PSGetPropertyDescriptionListFromString function (propsys.h)
description: Gets an instance of a property description list interface for a specified property list.
helpviewer_keywords: ["PSGetPropertyDescriptionListFromString","PSGetPropertyDescriptionListFromString function [Windows Properties]","properties.PSGetPropertyDescriptionListFromString","propsys/PSGetPropertyDescriptionListFromString","shell.PSGetPropertyDescriptionListFromString","shell_PSGetPropertyDescriptionListFromString"]
old-location: properties\PSGetPropertyDescriptionListFromString.htm
tech.root: properties
ms.assetid: 348253ed-46ac-4643-bbf8-2d286ae97f07
ms.date: 12/05/2018
ms.keywords: PSGetPropertyDescriptionListFromString, PSGetPropertyDescriptionListFromString function [Windows Properties], properties.PSGetPropertyDescriptionListFromString, propsys/PSGetPropertyDescriptionListFromString, shell.PSGetPropertyDescriptionListFromString, shell_PSGetPropertyDescriptionListFromString
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
req.dll: Propsys.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - PSGetPropertyDescriptionListFromString
 - propsys/PSGetPropertyDescriptionListFromString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PSGetPropertyDescriptionListFromString
---

# PSGetPropertyDescriptionListFromString function


## -description

Gets an instance of a property description list interface for a specified property list.

## -parameters

### -param pszPropList [in]

Type: <b>LPCWSTR</b>

Pointer to a null-terminated, Unicode string that identifies the property list. See <a href="/windows/desktop/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring">IPropertySystem::GetPropertyDescriptionListFromString</a> for more information about the format of this parameter.

### -param riid [in]

Type: <b>REFIID</b>

Reference to the interface ID of the requested interface.

### -param ppv [out]

Type: <b>void**</b>

When this function returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescriptionlist">IPropertyDescriptionList</a>.

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

This function calls the property subsystem implementation of <a href="/windows/desktop/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring">IPropertySystem::GetPropertyDescriptionListFromString</a> to obtain a collection of properties provided as a semicolon-delimited property list string.

We recommend that you use the <b>IID_PPV_ARGS</b> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error.

For more information about property schemas, see <a href="/windows/desktop/properties/building-property-handlers-property-schemas">Property Schemas</a>.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propsys/nf-propsys-psgetpropertydescriptionlistfromstring">PSGetPropertyDescriptionListFromString</a>.


```cpp
IPropertyDescriptionList *pList;

HRESULT hr = PSGetPropertyDescriptionListFromString(L"prop:System.Title;System.Size",
                                                    IID_PPV_ARGS(&pList));
                                                    
if (SUCCEEDED(hr))
{
    // pList is now valid.
 
    pList->Release();
}
```