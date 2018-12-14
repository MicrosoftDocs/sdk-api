---
UID: NF:propvarutil.PropVariantToInt64
title: PropVariantToInt64 function
author: windows-sdk-content
description: Extracts a LONGLONG value from a PROPVARIANT structure. If no value can be extracted, then a default value is assigned.
old-location: properties\PropVariantToInt64.htm
tech.root: properties
ms.assetid: a53c88e3-57cc-46f8-99f2-ffc2aafa0ce4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PropVariantToInt64, PropVariantToInt64 function [Windows Properties], properties.PropVariantToInt64, propvarutil/PropVariantToInt64, shell.PropVariantToInt64, shell_PropVariantToInt64
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
 - PropVariantToInt64
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# PropVariantToInt64 function


## -description


Extracts a <b>LONGLONG</b> value from a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure. If no value can be extracted, then a default value is assigned.


## -parameters




### -param propvarIn [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param pllRet [out]

Type: <b>LONGLONG*</b>

When this function returns, contains the extracted property value if one exists; otherwise, 0.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This helper function is used in places where the calling application expects a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> to hold an <b>LONGLONG</b> value. For instance, an application obtaining values from a property store can use this to safely extract the <b>LONGLONG</b> value for Int64 properties.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type <b>VT_I8</b>, this helper function extracts the <b>LONGLONG</b> value. Otherwise, it attempts to convert the value in the <b>PROPVARIANT</b> structure into a <b>LONGLONG</b>. If a conversion is not possible, <a href="shell.PropVariantToInt64">PropVariantToInt64</a> will return a failure code and set <i>pllRet</i> to 0. See <a href="shell.PropVariantChangeType">PropVariantChangeType</a> for a list of possible conversions. Of note, <b>VT_EMPTY</b> is successfully converted to 0.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// PROPVARIANT propvar;
// Assume the variable propvar is initialized and valid
LONGLONG llValue; // The application is expecting propvar to hold a VT_I8 value
HRESULT hr = PropVariantToInt64(propvar, &amp;llValue);
if (SUCCEEDED(hr))
{
     // llValue is valid
}                    
else
{
         // the extraction failed
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitPropVariantFromInt64">InitPropVariantFromInt64</a>



<a href="shell.PropVariantChangeType">PropVariantChangeType</a>



<a href="shell.PropVariantToInt64Vector">PropVariantToInt64Vector</a>



<a href="shell.VariantToInt64">VariantToInt64</a>
 

 

