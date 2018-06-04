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

# PropVariantToBoolean function


## -description


Extracts a Boolean property value of a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure. If no value can be extracted, then a default value is assigned.


## -parameters




### -param propvarIn [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param pfRet [out]

Type: <b>BOOL*</b>

When this function returns, contains the extracted property value if one exists; otherwise, contains <b>FALSE</b>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This helper function is used in places where the calling application expects a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> to hold a Boolean value. For instance, an application obtaining values from a property store can use this to safely extract the Boolean value for Boolean properties.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type <b>VT_BOOL</b>, this helper function extracts the Boolean value. Otherwise, it attempts to convert the value in the <b>PROPVARIANT</b> structure into a Boolean. If a conversion is not possible, <a href="shell.PropVariantToBoolean">PropVariantToBoolean</a> will return a failure code and set <i>pfRet</i> to <b>FALSE</b>. See <a href="shell.PropVariantChangeType">PropVariantChangeType</a> for a list of possible conversions. Of note, <b>VT_EMPTY</b> is successfully converted to <b>FALSE</b>.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.PropVariantToBoolean">PropVariantToBoolean</a> access a Boolean value in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// IPropertyStore *ppropstore;
// Assume variable ppropstore is initialized and valid
PROPVARIANT propvar = {0};

HRESULT hr = ppropstore-&gt;GetValue(PKEY_IsShared, &amp;propvar);
if (SUCCEEDED(hr))
{
     // PKEY_IsShared is expected to produce a VT_BOOL or VT_EMPTY value.
     // PropVariantToBoolean will convert VT_EMPTY to FALSE.
     BOOL fShared;
     
     hr = PropVariantToBoolean(propvar, &amp;fShared);
     if (SUCCEEDED(hr))
     {
         // fShared is now valid
     }
     else
     {
         // fShared is always FALSE
     }
     
     PropVariantClear(&amp;propvar);
}

                    </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitPropVariantFromBoolean">InitPropVariantFromBoolean</a>



<a href="shell.PropVariantGetBooleanElem">PropVariantGetBooleanElem</a>



<a href="shell.PropVariantToBooleanWithDefault">PropVariantToBooleanWithDefault</a>



<a href="shell.VariantToBoolean">VariantToBoolean</a>
 

 

