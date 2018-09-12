---
UID: NF:propvarutil.PropVariantToInt32
title: PropVariantToInt32 function
author: windows-sdk-content
description: Extracts the Int32 property value of a PROPVARIANT structure. If no value can be extracted, then a default value is assigned.
old-location: properties\PropVariantToInt32.htm
tech.root: properties
ms.assetid: 937722d6-cabf-4c4d-8ca9-06d6ed91b77a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PropVariantToInt32, PropVariantToInt32 function [Windows Properties], properties.PropVariantToInt32, propvarutil/PropVariantToInt32, shell.PropVariantToInt32, shell_PropVariantToInt32
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
 - PropVariantToInt32
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# PropVariantToInt32 function


## -description


Extracts the <b>Int32</b> property value of a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure. If no value can be extracted, then a default value is assigned.


## -parameters




### -param propvarIn [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param plRet [out]

Type: <b>LONG*</b>

When this function returns, contains the extracted value if one exists; otherwise, 0.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This helper function is used in places where the calling application expects a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> to hold an <b>Int32</b> value. For instance, an application obtaining values from a property store can use this to safely extract the <b>Int32</b> value for <b>Int32</b> properties.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type <b>VT_I4</b>, this helper function extracts the <b>long</b> value. Otherwise, it attempts to convert the value in the <b>PROPVARIANT</b> structure into a <b>long</b>. If a conversion is not possible, <a href="https://msdn.microsoft.com/en-us/library/Bb776550(v=VS.85).aspx">PropVariantToInt32</a> will return a failure code and set <i>plRet</i> to 0. See <a href="https://msdn.microsoft.com/en-us/library/Bb776514(v=VS.85).aspx">PropVariantChangeType</a> for a list of possible conversions. Of note, <b>VT_EMPTY</b> is successfully converted to 0.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// IPropertyStore *ppropstore;

// Assume variable ppropstore is initialized and valid

PROPVARIANT propvar = {0};

HRESULT hr = ppropstore-&gt;GetValue(PKEY_FlagStatus, &amp;propvar);

if (SUCCEEDED(hr))

{

     // PKEY_FlagStatus is expected to produce a VT_I4 or VT_EMPTY value.

     // PropVariantToInt32 will convert VT_EMPTY to 0.

     INT32 iStatus;

     hr = PropVariantToInt32(propvar, &amp;iStatus);

     if (SUCCEEDED(hr))

     {

             // iStatus is now valid

     }

     else

     {

             // iStatus is always 0

     }

     PropVariantClear(&amp;propvar);

}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb762299(v=VS.85).aspx">InitPropVariantFromInt32</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776514(v=VS.85).aspx">PropVariantChangeType</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776551(v=VS.85).aspx">PropVariantToInt32Vector</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776608(v=VS.85).aspx">VariantToInt32</a>
 

 

