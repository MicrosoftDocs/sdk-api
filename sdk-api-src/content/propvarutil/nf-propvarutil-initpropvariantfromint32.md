---
UID: NF:propvarutil.InitPropVariantFromInt32
title: InitPropVariantFromInt32 function
author: windows-sdk-content
description: Initializes a PROPVARIANT structure based on a 32-bit integer value.
old-location: properties\InitPropVariantFromInt32.htm
old-project: properties
ms.assetid: 923be4ac-5545-431b-ab69-3b7f366a1ec0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: InitPropVariantFromInt32, InitPropVariantFromInt32 function [Windows Properties], properties.InitPropVariantFromInt32, propvarutil/InitPropVariantFromInt32, shell.InitPropVariantFromInt32, shell_InitPropVariantFromInt32
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
 - HeaderDef
api_location:
 - Propvarutil.h
api_name:
 - InitPropVariantFromInt32
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# InitPropVariantFromInt32 function


## -description


Initializes a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure based on a 32-bit integer value.


## -parameters




### -param lVal [in]

Type: <b>LONG</b>

The source <b>LONG</b> value.


### -param ppropvar [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a VT_I4 propvariant.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.InitPropVariantFromInt32">InitPropVariantFromInt32</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromInt32(127, &amp;propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_I4.
 
    PropVariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitVariantFromInt32">InitVariantFromInt32</a>



<a href="shell.PropVariantToInt32">PropVariantToInt32</a>



<a href="shell.PropVariantToInt32WithDefault">PropVariantToInt32WithDefault</a>
 

 

