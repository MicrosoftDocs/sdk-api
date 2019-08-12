---
UID: NF:propsys.PSSetPropertyValue
title: PSSetPropertyValue function (propsys.h)
author: windows-sdk-content
description: Sets the value of a property in a property store.
old-location: properties\PSSetPropertyValue.htm
tech.root: properties
ms.assetid: b4f8c50d-93cd-4371-88b0-6ce58f023981
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PSSetPropertyValue, PSSetPropertyValue function [Windows Properties], _shell_PSSetPropertyValue, properties.PSSetPropertyValue, propsys/PSSetPropertyValue, shell.PSSetPropertyValue
ms.topic: function
f1_keywords:
- propsys/PSSetPropertyValue
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
- PSSetPropertyValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# PSSetPropertyValue function


## -description


Sets the value of a property in a property store.


## -parameters




### -param pps [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>*</b>

Pointer to an instance of the <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> interface, which represents the property store that contains the property.


### -param ppd [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a>*</b>

Pointer to an instance of the <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a> interface, which identifies the individual property.


### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure that contains the new value.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This helper function is used to write a property value to a store. If the calling code already has a <a href="https://docs.microsoft.com/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure, it might be simpler to call <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-ipropertystore-setvalue">IPropertyStore::SetValue</a> directly.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-pssetpropertyvalue">PSSetPropertyValue</a>.


```cpp
// IPropertyDescription *pPropDesc;
// IPropertyStore *pStore;
// PROPVARIANT propvar;
// Assume the variables pStore, pPropDesc, and propvar are initialized and valid.

HRESULT hr = PSSetPropertyValue(pStore, pPropDesc, propvar);

if (SUCCEEDED(hr))
{
    // The value has been written to the store but has not been committed yet.
}
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-ipropertystore-commit">IPropertyStore::Commit</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-psgetpropertyvalue">PSGetPropertyValue</a>
 

 

