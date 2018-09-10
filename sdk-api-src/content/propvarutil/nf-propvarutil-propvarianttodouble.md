---
UID: NF:propvarutil.PropVariantToDouble
title: PropVariantToDouble function
author: windows-sdk-content
description: Extracts double value from a PROPVARIANT structure.
old-location: properties\PropVariantToDouble.htm
tech.root: properties
ms.assetid: 346b3f37-1279-4719-b1cd-50adf4d070f0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PropVariantToDouble, PropVariantToDouble function [Windows Properties], properties.PropVariantToDouble, propvarutil/PropVariantToDouble, shell.PropVariantToDouble, shell_PropVariantToDouble
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
 - PropVariantToDouble
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# PropVariantToDouble function


## -description


Extracts double value from a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -parameters




### -param propvarIn [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param pdblRet [out]

Type: <b>DOUBLE*</b>

When this function returns, contains the extracted property value if one exists; otherwise, contains 0.0.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This helper function is used in places where the calling application expects a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> to hold a single double floating point value. For instance, an application obtaining values from a property store can use this to safely extract a double value for double properties.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type <b>VT_R8</b>, this helper function extracts the double value. Otherwise, it attempts to convert the value in the <b>PROPVARIANT</b> structure into a double. If a conversion is not possible, <a href="https://msdn.microsoft.com/en-us/library/Bb776538(v=VS.85).aspx">PropVariantToDouble</a> will return a failure code and set <i>pdblRet</i> to 0.0. See <a href="https://msdn.microsoft.com/en-us/library/Bb776514(v=VS.85).aspx">PropVariantChangeType</a> for a list of possible conversions. Of note, <b>VT_EMPTY</b> is successfully converted to 0.0.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use PropVariantToDouble to access a double value in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// IPropertyStore *ppropstore;
// Assume variable ppropstore is initialized and valid
PROPVARIANT propvar = {0};
HRESULT hr = ppropstore-&gt;GetValue(PKEY_Image_HorizontalResolution, &amp;propvar);
if (SUCCEEDED(hr))
{
     // PKEY_Image_HorizontalResolution is expected to produce a VT_R8 or VT_EMPTY value.
     // PropVariantToDouble will successfully convert VT_EMPTY to a 0.0.
     DOUBLE dblHorzResolution;
     hr = PropVariantToDouble(propvar, &amp;dblHorzResolution);
     if (SUCCEEDED(hr))
     {
        // dblHorzResolution is now valid
     }
     else
     {
        // dblHorzResolution contains 0.0
     }
     PropVariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb762291(v=VS.85).aspx">InitPropVariantFromDouble</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776520(v=VS.85).aspx">PropVariantGetDoubleElem</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776541(v=VS.85).aspx">PropVariantToDoubleWithDefault</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776598(v=VS.85).aspx">VariantToDouble</a>
 

 

