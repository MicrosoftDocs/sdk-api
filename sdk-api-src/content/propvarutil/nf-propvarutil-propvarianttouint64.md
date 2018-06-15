---
UID: NF:propvarutil.PropVariantToUInt64
title: PropVariantToUInt64 function
author: windows-sdk-content
description: Extracts a UInt64 value from a PROPVARIANT structure. If no value can be extracted, then a default value is assigned.
old-location: properties\PropVariantToUInt64.htm
old-project: properties
ms.assetid: 3a6bdfb0-eae1-40e7-85c1-234732a4bc3f
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PropVariantToUInt64, PropVariantToUInt64 function [Windows Properties], properties.PropVariantToUInt64, propvarutil/PropVariantToUInt64, shell.PropVariantToUInt64, shell_PropVariantToUInt64
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PropVariantToUInt64
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PropVariantToUInt64 function


## -description


Extracts a <b>UInt64</b> value from a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure. If no value can be extracted, then a default value is assigned.


## -parameters




### -param propvarIn [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param pullRet [out]

Type: <b>ULONGLONG*</b>

When this function returns, contains the extracted property value if one exists; otherwise, 0.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This helper function is used in places where the calling application expects a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> to hold a <b>ULONGLONG</b> value. For instance, an application obtaining values from a property store can use this to safely extract the <b>ULONGLONG</b>  value for <b>UInt64</b> properties.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type <b>VT_UI8</b>, this helper function extracts the <b>ULONGLONG</b>  value. Otherwise, it attempts to convert the value in the <b>PROPVARIANT</b> structure into a <b>ULONGLONG</b>. If a conversion is not possible, <a href="https://www.bing.com/search?q=PropVariantToUInt64">PropVariantToUInt64</a> will return a failure code and set <i>pullRet</i> to 0. See <a href="https://www.bing.com/search?q=PropVariantChangeType">PropVariantChangeType</a> for a list of possible conversions. Of note, <b>VT_EMPTY</b> is successfully converted to 0.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://www.bing.com/search?q=PropVariantToUInt64">PropVariantToUInt64</a> to access a <b>ULONGLONG</b> value in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// IPropertyStore *ppropstore;

// Assume variable ppropstore is initialized and valid

PROPVARIANT propvar = {0};

HRESULT hr = ppropstore-&gt;GetValue(PKEY_Size, &amp;propvar);

if (SUCCEEDED(hr))

{

     // PKEY_Size is expected to produce a VT_UI8 or VT_EMPTY value.

     // PropVariantToUInt64 will convert VT_EMPTY to 0.

     ULONGLONG ullSize;

     hr = PropVariantToUInt64(propvar, &amp;ullSize);

     if (SUCCEEDED(hr))

     {

             // ullSize is now valid

     }

     else

     {

             // ullSize is always 0

     }

     PropVariantClear(&amp;propvar);

}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://www.bing.com/search?q=InitPropVariantFromUInt64">InitPropVariantFromUInt64</a>



<a href="https://www.bing.com/search?q=PropVariantChangeType">PropVariantChangeType</a>



<a href="https://www.bing.com/search?q=PropVariantToUInt64Vector">PropVariantToUInt64Vector</a>



<a href="https://www.bing.com/search?q=VariantToUInt64">VariantToUInt64</a>
 

 

