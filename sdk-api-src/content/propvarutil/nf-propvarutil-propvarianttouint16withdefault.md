---
UID: NF:propvarutil.PropVariantToUInt16WithDefault
title: PropVariantToUInt16WithDefault function
author: windows-sdk-content
description: Extracts an unsigned short value from a PROPVARIANT structure. If no value exists, then the specified default value is returned.
old-location: properties\PropVariantToUInt16WithDefault.htm
old-project: properties
ms.assetid: 4346cef2-5e43-47bf-9bfb-0ede923872fd
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PropVariantToUInt16WithDefault, PropVariantToUInt16WithDefault function [Windows Properties], properties.PropVariantToUInt16WithDefault, propvarutil/PropVariantToUInt16WithDefault, shell.PropVariantToUInt16WithDefault, shell_PropVariantToUInt16WithDefault
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
 - PropVariantToUInt16WithDefault
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: ADAM
---

# PropVariantToUInt16WithDefault function


## -description


Extracts an <b>unsigned short</b> value from a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure. If no value exists, then the specified default value is returned.


## -parameters




### -param propvarIn [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param uiDefault [in]

Type: <b>USHORT</b>

Specifies a default property value, for use where no value currently exists.


## -returns



Type: <b>unsigned short</b>

Returns extracted <b>unsigned short</b> value, or default.




## -remarks



This helper function is used in places where the calling application expects a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> to hold a  <b>unsigned short</b>   value. For instance, an application obtaining values from a property store can use this to safely extract the  <b>unsigned short</b>  value for UInt16 properties.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type <b>VT_UI2</b>, this helper function extracts the <b>unsigned short</b> value. Otherwise, it attempts to convert the value in the <b>PROPVARIANT</b> structure into a <b>unsigned short</b>. If a conversion is not possible, <a href="https://msdn.microsoft.com/library/Bb776565(v=VS.85).aspx">PropVariantToUInt16</a> will return a failure code and set <i>puiRet</i> to 0. See <a href="https://msdn.microsoft.com/library/Bb776514(v=VS.85).aspx">PropVariantChangeType</a> for a list of possible conversions. Of note, <b>VT_EMPTY</b> is successfully converted to 0.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/library/Bb776565(v=VS.85).aspx">PropVariantToUInt16</a> to access a <b>unsigned short</b> value in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// IPropertyStore *ppropstore;

// Assume variable ppropstore is initialized and valid

PROPVARIANT propvar = {0};

HRESULT hr = ppropstore-&gt;GetValue(PKEY_FlagColor, &amp;propvar);

if (SUCCEEDED(hr))

{

     // PKEY_FlagColor is expected to produce a VT_UI2 or VT_EMPTY value.

     // PropVariantToInt32 will convert VT_EMPTY to 0.

     USHORT uColor;

     hr = PropVariantToUInt32(propvar, &amp; uColor);

     if (SUCCEEDED(hr))

     {

             // uColor is now valid

     }

     else

     {

             // uColor is always 0

     }

     PropVariantClear(&amp;propvar);

}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/Bb762309(v=VS.85).aspx">InitPropVariantFromUInt16</a>



<a href="https://msdn.microsoft.com/library/Bb776514(v=VS.85).aspx">PropVariantChangeType</a>



<a href="https://msdn.microsoft.com/library/Bb776566(v=VS.85).aspx">PropVariantToUInt16Vector</a>



<a href="https://msdn.microsoft.com/library/Bb776623(v=VS.85).aspx">VariantToUInt16</a>
 

 

