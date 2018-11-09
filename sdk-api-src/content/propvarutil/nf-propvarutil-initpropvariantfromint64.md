---
UID: NF:propvarutil.InitPropVariantFromInt64
title: InitPropVariantFromInt64 function
author: windows-sdk-content
description: Initializes a PROPVARIANT structure based on a specified Int64 value.
old-location: properties\InitPropVariantFromInt64.htm
tech.root: properties
ms.assetid: 2a2a5348-4d3d-475c-8039-097b4dacf7cb
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: InitPropVariantFromInt64, InitPropVariantFromInt64 function [Windows Properties], properties.InitPropVariantFromInt64, propvarutil/InitPropVariantFromInt64, shell.InitPropVariantFromInt64, shell_InitPropVariantFromInt64
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
 - InitPropVariantFromInt64
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# InitPropVariantFromInt64 function


## -description


Initializes a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure based on a specified <b>Int64</b> value.


## -parameters




### -param llVal [in]

Type: <b>LONGLONG</b>

The source <b>LONGLONG</b> value.


### -param ppropvar [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a VT_I8 propvariant.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/en-us/library/Bb762301(v=VS.85).aspx">InitPropVariantFromInt64</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromInt64(4096, &amp;propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_I8.
 
    PropVariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb762331(v=VS.85).aspx">InitVariantFromInt64</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776554(v=VS.85).aspx">PropVariantToInt64</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776558(v=VS.85).aspx">PropVariantToInt64WithDefault</a>
 

 

