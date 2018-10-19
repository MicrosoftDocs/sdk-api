---
UID: NF:propvarutil.InitVariantFromDouble
title: InitVariantFromDouble function
author: windows-sdk-content
description: Initializes a VARIANT structure with a value of type DOUBLE.
old-location: properties\InitVariantFromDouble.htm
tech.root: properties
ms.assetid: a0a13843-e943-4fca-b4d4-5af1d2ff02e9
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: InitVariantFromDouble, InitVariantFromDouble function [Windows Properties], _shell_InitVariantFromDouble, properties.InitVariantFromDouble, propvarutil/InitVariantFromDouble, shell.InitVariantFromDouble
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Propvarutil.h
api_name:
 - InitVariantFromDouble
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# InitVariantFromDouble function


## -description


Initializes a <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> structure with a value of type DOUBLE.


## -parameters




### -param dblVal [in]

Type: <b>DOUBLE</b>

Source value.


### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a VT_R8 variant.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.InitVariantFromDouble">InitVariantFromDouble</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VARIANT var;

HRESULT hr = InitVariantFromDouble(3.1415, &amp;var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_R8.
    VariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitPropVariantFromDouble">InitPropVariantFromDouble</a>



<a href="shell.VariantToDouble">VariantToDouble</a>



<a href="shell.VariantToDoubleWithDefault">VariantToDoubleWithDefault</a>
 

 

