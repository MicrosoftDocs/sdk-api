---
UID: NF:propvarutil.PropVariantGetBooleanElem
title: PropVariantGetBooleanElem function
author: windows-driver-content
description: Extracts a single Boolean element from a PROPVARIANT structure of type VT_BOOL, VT_VECTOR | VT_BOOL, or VT_ARRAY | VT_BOOL.
old-location: properties\PropVariantGetBooleanElem.htm
old-project: properties
ms.assetid: 830dca70-1777-418d-b3ac-78028411700e
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: PropVariantGetBooleanElem, PropVariantGetBooleanElem function [Windows Properties], _shell_PropVariantGetBooleanElem, properties.PropVariantGetBooleanElem, propvarutil/PropVariantGetBooleanElem, shell.PropVariantGetBooleanElem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: propvarutil.h
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
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Propsys.dll
api_name:
-	PropVariantGetBooleanElem
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PropVariantGetBooleanElem function


## -description


Extracts a single Boolean element from a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure of type <code>VT_BOOL</code>, <code>VT_VECTOR | VT_BOOL</code>, or <code>VT_ARRAY | VT_BOOL</code>.


## -parameters




### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

A reference to the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param iElem [in]

Type: <b>ULONG</b>

Specifies the vector or array index; otherwise, <i>iElem</i> must be 0.


### -param pfVal [out]

Type: <b>BOOL*</b>

When this function returns, contains the extracted Boolean value.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure has type <code>VT_BOOL</code>, <i>iElem</i> must be 0. Otherwise <i>iElem</i> must be less than the number of elements in the vector or array. You can use <a href="shell.PropVariantGetElementCount">PropVariantGetElementCount</a> to obtain the number of elements in the vector or array.

The following example uses this function to loop through the values in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// PROPVARIANT propvar;
// assume propvar is initialized and valid

if ((propvar.vt &amp; VT_TYPEMASK) == VT_BOOL)
{
    UINT cElem = PropVariantGetElementCount(propvar);
    HRESULT hr = &lt;mark type="const"&gt;S_OK&lt;/mark&gt;;
    
    for (UINT iElem = 0; SUCCEEDED(hr) &amp;&amp; iElem &lt; cElem; iElem ++)
    {
        BOOL fValue;
        hr = PropVariantGetBooleanElem(propvar, iElem, &amp;fValue);
    
        if (SUCCEEDED(hr))
        {
            // fValue is valid now
        }
    }
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.PropVariantGetElem">PropVariantGetElem</a>
 

 

