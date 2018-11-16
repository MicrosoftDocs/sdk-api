---
UID: NF:propvarutil.PropVariantToInt64WithDefault
title: PropVariantToInt64WithDefault function
author: windows-sdk-content
description: Extracts the Int64 property value of a PROPVARIANT structure. If no value exists, then specified default value is returned.
old-location: properties\PropVariantToInt64WithDefault.htm
tech.root: properties
ms.assetid: 6a051235-3e32-40d3-a17e-efc571592dae
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: PropVariantToInt64WithDefault, PropVariantToInt64WithDefault function [Windows Properties], properties.PropVariantToInt64WithDefault, propvarutil/PropVariantToInt64WithDefault, shell.PropVariantToInt64WithDefault, shell_PropVariantToInt64WithDefault
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
 - PropVariantToInt64WithDefault
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
- apiref
: 
- 
: 
- PropVariantToInt64WithDefault
: 
---

# PropVariantToInt64WithDefault function


## -description


Extracts the <b>Int64</b> property value of a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure. If no value exists, then specified default value is returned.


## -parameters




### -param propvarIn [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param llDefault [in]

Type: <b>LONGLONG</b>

Specifies a default property value, for use where no value currently exists.


## -returns



Type: <b>LONGLONG</b>

Returns the extracted <b>LONGLONG</b> value, or default.




## -remarks



This helper function is used in places where the calling application expects a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> to hold a <b>LONGLONG</b> value and would like to use a default value if it does not. For instance, an application obtaining values from a property store can use this to safely extract the <b>LONGLONG</b> value for Int64 properties.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type <b>VT_I8</b>, this helper function extracts the <b>LONGLONG</b> value. Otherwise, it attempts to convert the value in the <b>PROPVARIANT</b> structure into a <b>LONGLONG</b>. If the source <b>PROPVARIANT</b> has type <b>VT_EMPTY</b> or a conversion is not possible, then <a href="shell.PropVariantToInt64WithDefault">PropVariantToInt64WithDefault</a> will return the default provided by <i>llDefault</i>. See <a href="shell.PropVariantChangeType">PropVariantChangeType</a> for a list of possible conversions.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.PropVariantToInt64WithDefault">PropVariantToInt64WithDefault</a> to access a <b>LONGLONG</b> value in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// PROPVARIANT propvar;
// Assume the variable propvar is initialized and valid
// The application is expecting propvar to hold a VT_I8 value, but wishes to treat VT_EMPTY as -1.
LONGLONG llValue = PropVariantToInt64WithDefault(propvar, -1);
// llValue is valid</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitPropVariantFromInt64">InitPropVariantFromInt64</a>



<a href="shell.PropVariantChangeType">PropVariantChangeType</a>



<a href="shell.PropVariantToInt64">PropVariantToInt64</a>



<a href="shell.VariantToInt64">VariantToInt64</a>
 

 

