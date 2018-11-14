---
UID: NF:propvarutil.InitPropVariantFromUInt64
title: InitPropVariantFromUInt64 function
author: windows-sdk-content
description: Initializes a PROPVARIANT structure with a 64-bit unsigned integer value.
old-location: properties\InitPropVariantFromUInt64.htm
tech.root: properties
ms.assetid: c0dbc8d1-45ed-497b-a6ef-2beb4f031e4b
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: InitPropVariantFromUInt64, InitPropVariantFromUInt64 function [Windows Properties], properties.InitPropVariantFromUInt64, propvarutil/InitPropVariantFromUInt64, shell.InitPropVariantFromUInt64, shell_InitPropVariantFromUInt64
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
 - InitPropVariantFromUInt64
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
- apiref
: 
- 
: 
- InitPropVariantFromUInt64
: 
---

# InitPropVariantFromUInt64 function


## -description


Initializes a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure with a 64-bit unsigned integer value.


## -parameters




### -param ullVal [in]

Type: <b>ULONGLONG</b>

Source <b>ULONGLONG</b> value.


### -param ppropvar [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a VT_UI8 propvariant.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.InitPropVariantFromUInt64">InitPropVariantFromUInt64</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromUInt64(563, &amp;propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_UI8.
    PropVariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitVariantFromUInt64">InitVariantFromUInt64</a>



<a href="shell.PropVariantToUInt64">PropVariantToUInt64</a>



<a href="shell.PropVariantToUInt64WithDefault">PropVariantToUInt64WithDefault</a>
 

 

