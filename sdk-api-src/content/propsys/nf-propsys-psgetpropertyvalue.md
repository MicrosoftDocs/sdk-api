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

# PSGetPropertyValue function


## -description


Gets a property value from a property store.


## -parameters




### -param pps [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a>*</b>

Pointer to an instance of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> interface, which represents the property store from which to get the value.


### -param ppd [in]

Type: <b><a href="shell.IPropertyDescription">IPropertyDescription</a>*</b>

Pointer to an instance of the <a href="shell.IPropertyDescription">IPropertyDescription</a> interface, which represents the property in the property store.


### -param ppropvar [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

Pointer to an uninitialized <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure. When this function returns, points to the requested property value.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This helper function is used to read a property value from a store. If the calling code already has a <a href="shell.PROPERTYKEY">PROPERTYKEY</a> structure, it might be simpler to call <a href="https://msdn.microsoft.com/library/windows/hardware/ff536962">IPropertyStore::GetValue</a> directly.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.PSGetPropertyValue">PSGetPropertyValue</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// IPropertyDescription *pPropDesc;
// IPropertyStore *pStore;
// Assume the variables pPropDesc and pStore are initialized and valid.
PROPVARIANT propvar;

HRESULT hr = PSGetPropertyValue(pStore, pPropDesc, &amp;propvar);

if (SUCCEEDED(hr))
{
    // propvar is valid.
 
    PropVariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.PSSetPropertyValue">PSSetPropertyValue</a>
 

 

