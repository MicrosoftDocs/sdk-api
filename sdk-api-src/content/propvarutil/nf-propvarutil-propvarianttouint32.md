---
UID: NF:propvarutil.PropVariantToUInt32
title: PropVariantToUInt32 function
author: windows-sdk-content
description: Extracts an ULONG value from a PROPVARIANT structure. If no value can be extracted, then a default value is assigned.
old-location: properties\PropVariantToUInt32.htm
old-project: properties
ms.assetid: ce1d8d07-2532-48bd-be8b-7650230dbe0d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PropVariantToUInt32, PropVariantToUInt32 function [Windows Properties], properties.PropVariantToUInt32, propvarutil/PropVariantToUInt32, shell.PropVariantToUInt32, shell_PropVariantToUInt32
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: propvarutil.h
req.include-header: 
req.redist: Windows Desktop Search (WDS) 3.0
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
 - PropVariantToUInt32
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: ADAM
---

# PropVariantToUInt32 function


## -description


Extracts an <b>ULONG</b> value from a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure. If no value can be extracted, then a default value is assigned.


## -parameters




### -param propvarIn [in]

Type: <b>REFPROPVARIANT</b>

A reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param pulRet [out]

Type: <b>ULONG*</b>

When this function returns, contains the extracted property value if one exists; otherwise, 0.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This helper function is used in places where the calling application expects a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> to hold a <b>ULONG</b> value. For instance, an application obtaining values from a property store can use this to safely extract the <b>ULONG</b>  value for UInt32 properties.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type <b>VT_UI4</b>, this helper function extracts the <b>ULONG</b> value. Otherwise, it attempts to convert the value in the <b>PROPVARIANT</b> structure into a <b>ULONG</b>. If a conversion is not possible, <a href="shell.PropVariantToUInt32">PropVariantToUInt32</a> will return a failure code and set <i>pulRet</i> to 0. See <a href="shell.PropVariantChangeType">PropVariantChangeType</a> for a list of possible conversions. Of note, <b>VT_EMPTY</b> is successfully converted to 0.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.PropVariantToUInt32">PropVariantToUInt32</a> to access a <b>ULONG</b> value in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// IPropertyStore *ppropstore;

// Assume variable ppropstore is initialized and valid

PROPVARIANT propvar = {0};

HRESULT hr = ppropstore-&gt;GetValue(PKEY_Rating, &amp;propvar);

if (SUCCEEDED(hr))

{

     // PKEY_Rating is expected to produce a VT_UI4 or VT_EMPTY value.

     // PropVariantToUInt32 will convert VT_EMPTY to 0.

     ULONG uRating;

     hr = PropVariantToUInt32(propvar, &amp;uRating);

     if (SUCCEEDED(hr))

     {

             // uRating is now valid

     }

     else

     {

             // uRating is always 0

     }

     PropVariantClear(&amp;propvar);

}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitPropVariantFromUInt32">InitPropVariantFromUInt32</a>



<a href="shell.PropVariantChangeType">PropVariantChangeType</a>



<a href="shell.PropVariantToUInt32Vector">PropVariantToUInt32Vector</a>



<a href="shell.VariantToUInt32">VariantToUInt32</a>
 

 

