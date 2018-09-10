---
UID: NF:propsys.PSGetPropertyValue
title: PSGetPropertyValue function
author: windows-sdk-content
description: Gets a property value from a property store.
old-location: properties\PSGetPropertyValue.htm
tech.root: properties
ms.assetid: 9369dc85-b006-4b30-a25e-58d53b76f334
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PSGetPropertyValue, PSGetPropertyValue function [Windows Properties], _shell_PSGetPropertyValue, properties.PSGetPropertyValue, propsys/PSGetPropertyValue, shell.PSGetPropertyValue
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
 - PSGetPropertyValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# PSGetPropertyValue function


## -description


Gets a property value from a property store.


## -parameters




### -param pps [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb761474(v=VS.85).aspx">IPropertyStore</a>*</b>

Pointer to an instance of the <a href="https://msdn.microsoft.com/en-us/library/Bb761474(v=VS.85).aspx">IPropertyStore</a> interface, which represents the property store from which to get the value.


### -param ppd [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb761561(v=VS.85).aspx">IPropertyDescription</a>*</b>

Pointer to an instance of the <a href="https://msdn.microsoft.com/en-us/library/Bb761561(v=VS.85).aspx">IPropertyDescription</a> interface, which represents the property in the property store.


### -param ppropvar [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

Pointer to an uninitialized <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure. When this function returns, points to the requested property value.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This helper function is used to read a property value from a store. If the calling code already has a <a href="https://msdn.microsoft.com/en-us/library/Bb773381(v=VS.85).aspx">PROPERTYKEY</a> structure, it might be simpler to call <a href="https://msdn.microsoft.com/en-us/library/Ff536962(v=VS.85).aspx">IPropertyStore::GetValue</a> directly.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/en-us/library/Bb762083(v=VS.85).aspx">PSGetPropertyValue</a>.

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




<a href="https://msdn.microsoft.com/en-us/library/Bb762088(v=VS.85).aspx">PSSetPropertyValue</a>
 

 

