---
UID: NF:propvarutil.InitPropVariantFromBoolean
title: InitPropVariantFromBoolean function
author: windows-driver-content
description: Initializes a given PROPVARIANT structure as a VT_BOOL using a specified Boolean value.
old-location: properties\InitPropVariantFromBoolean.htm
old-project: properties
ms.assetid: aa23f7a2-1983-4a30-b2fc-601efa37e0ff
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: InitPropVariantFromBoolean, InitPropVariantFromBoolean function [Windows Properties], properties.InitPropVariantFromBoolean, propvarutil/InitPropVariantFromBoolean, shell.InitPropVariantFromBoolean, shell_InitPropVariantFromBoolean
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
-	HeaderDef
api_location:
-	Propvarutil.h
api_name:
-	InitPropVariantFromBoolean
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# InitPropVariantFromBoolean function


## -description


Initializes a given <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure as a <b>VT_BOOL</b> using a specified Boolean value.


## -parameters




### -param fVal [in]

Type: <b>BOOL</b>

Source <b>BOOL</b> value.


### -param ppropvar [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.

Note that the <i>boolVal</i> member specifically initialized by this function is of type <b>VARIANT_BOOL</b> and therefore can have values <b>VARIANT_TRUE</b> or <b>VARIANT_FALSE</b>. When working with this structure member directly, use these constants instead of <b>TRUE</b> or <b>FALSE</b> because <b>VARIANT_TRUE</b> is not equal to <b>TRUE</b> and sizeof(<b>VARIANT_TRUE</b>) is not the same as sizeof(<b>TRUE</b>).


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.InitPropVariantFromBoolean">InitPropVariantFromBoolean</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromBoolean(TRUE, &amp;propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_BOOL.
 
    PropVariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitPropVariantFromBooleanVector">InitPropVariantFromBooleanVector</a>



<a href="shell.InitVariantFromBoolean">InitVariantFromBoolean</a>



<a href="shell.PropVariantToBoolean">PropVariantToBoolean</a>
 

 

