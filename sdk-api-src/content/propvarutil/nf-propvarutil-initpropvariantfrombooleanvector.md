---
UID: NF:propvarutil.InitPropVariantFromBooleanVector
title: InitPropVariantFromBooleanVector function
author: windows-sdk-content
description: Initializes a PROPVARIANT structure from a specified Boolean vector.
old-location: properties\InitPropVariantFromBooleanVector.htm
old-project: properties
ms.assetid: d2e34efb-d5d9-4adf-b582-d3f82d04597f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: InitPropVariantFromBooleanVector, InitPropVariantFromBooleanVector function [Windows Properties], _shell_InitPropVariantFromBooleanVector, properties.InitPropVariantFromBooleanVector, propvarutil/InitPropVariantFromBooleanVector, shell.InitPropVariantFromBooleanVector
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
 - InitPropVariantFromBooleanVector
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: ADAM
---

# InitPropVariantFromBooleanVector function


## -description


Initializes a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure from a specified Boolean vector.


## -parameters




### -param prgf [in, optional]

Type: <b>const BOOL*</b>

Pointer to the Boolean vector used to initialize the structure. If this parameter is <b>NULL</b>, the elements pointed to by the <b>cabool.pElems</b> structure member are initialized with VARIANT_FALSE.


### -param cElems [in]

Type: <b>ULONG</b>

The number of vector elements.


### -param ppropvar [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This creates a <b>VT_BOOL</b> | <b>VT_VECTOR</b> propvariant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/en-us/library/Bb762288(v=VS.85).aspx">InitPropVariantFromBooleanVector</a>


<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>PROPVARIANT propvar;
BOOL rgBool[2] = {TRUE, FALSE};

HRESULT hr = InitPropVariantFromBooleanVector(rgBool, ARRAYSIZE(rgBool), &amp;propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_VECTOR | VT_BOOL.
 
    PropVariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb762287(v=VS.85).aspx">InitPropVariantFromBoolean</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb762316(v=VS.85).aspx">InitVariantFromBoolean</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776532(v=VS.85).aspx">PropVariantToBooleanVector</a>
 

 

