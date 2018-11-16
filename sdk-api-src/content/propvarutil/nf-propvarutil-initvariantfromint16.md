---
UID: NF:propvarutil.InitVariantFromInt16
title: InitVariantFromInt16 function
author: windows-sdk-content
description: Initializes a VARIANT structure with a 16-bit integer value.
old-location: properties\InitVariantFromInt16.htm
tech.root: properties
ms.assetid: 8ccb09bf-a2d2-4637-b8b1-e7abe83b846d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: InitVariantFromInt16, InitVariantFromInt16 function [Windows Properties], _shell_InitVariantFromInt16, properties.InitVariantFromInt16, propvarutil/InitVariantFromInt16, shell.InitVariantFromInt16
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
 - InitVariantFromInt16
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
- apiref
: 
- 
: 
- InitVariantFromInt16
: 
---

# InitVariantFromInt16 function


## -description


Initializes a <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> structure with a 16-bit integer value.


## -parameters




### -param iVal [in]

Type: <b>SHORT</b>

Source <b>SHORT</b> value.


### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a VT_I2 variant.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.InitVariantFromInt16">InitVariantFromInt16</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VARIANT var;

HRESULT hr = InitVariantFromInt16(3, &amp;var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_I2.
    VariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitPropVariantFromInt16">InitPropVariantFromInt16</a>



<a href="shell.VariantToInt16">VariantToInt16</a>



<a href="shell.VariantToInt16WithDefault">VariantToInt16WithDefault</a>
 

 

