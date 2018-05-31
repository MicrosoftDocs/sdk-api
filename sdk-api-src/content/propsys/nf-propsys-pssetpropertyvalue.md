---
UID: NF:propsys.PSSetPropertyValue
title: PSSetPropertyValue function
author: windows-sdk-content
description: Sets the value of a property in a property store.
old-location: properties\PSSetPropertyValue.htm
old-project: properties
ms.assetid: b4f8c50d-93cd-4371-88b0-6ce58f023981
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PSSetPropertyValue, PSSetPropertyValue function [Windows Properties], _shell_PSSetPropertyValue, properties.PSSetPropertyValue, propsys/PSSetPropertyValue, shell.PSSetPropertyValue
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: PSC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Propsys.dll
api_name:
-	PSSetPropertyValue
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PSSetPropertyValue function


## -description


Sets the value of a property in a property store.


## -parameters




### -param pps [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a>*</b>

Pointer to an instance of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> interface, which represents the property store that contains the property.


### -param ppd [in]

Type: <b><a href="shell.IPropertyDescription">IPropertyDescription</a>*</b>

Pointer to an instance of the <a href="shell.IPropertyDescription">IPropertyDescription</a> interface, which identifies the individual property.


### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure that contains the new value.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This helper function is used to write a property value to a store. If the calling code already has a <a href="shell.PROPERTYKEY">PROPERTYKEY</a> structure, it might be simpler to call <a href="https://msdn.microsoft.com/library/windows/hardware/ff536963">IPropertyStore::SetValue</a> directly.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.PSSetPropertyValue">PSSetPropertyValue</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// IPropertyDescription *pPropDesc;
// IPropertyStore *pStore;
// PROPVARIANT propvar;
// Assume the variables pStore, pPropDesc, and propvar are initialized and valid.

HRESULT hr = PSSetPropertyValue(pStore, pPropDesc, propvar);

if (SUCCEEDED(hr))
{
    // The value has been written to the store but has not been committed yet.
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536957">IPropertyStore::Commit</a>



<a href="shell.PSGetPropertyValue">PSGetPropertyValue</a>
 

 

