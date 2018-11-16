---
UID: NF:propvarutil.InitPropVariantFromUInt32
title: InitPropVariantFromUInt32 function
author: windows-sdk-content
description: Initializes a PROPVARIANT structure based on a 32-bit unsigned integer value.
old-location: properties\InitPropVariantFromUInt32.htm
tech.root: properties
ms.assetid: 38fb5226-7916-49b5-9e8e-bfd2f0cfd22a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: InitPropVariantFromUInt32, InitPropVariantFromUInt32 function [Windows Properties], properties.InitPropVariantFromUInt32, propvarutil/InitPropVariantFromUInt32, shell.InitPropVariantFromUInt32, shell_InitPropVariantFromUInt32
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
 - InitPropVariantFromUInt32
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
- apiref
: 
- 
: 
- InitPropVariantFromUInt32
: 
---

# InitPropVariantFromUInt32 function


## -description


Initializes a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure based on a 32-bit unsigned integer value.


## -parameters




### -param ulVal [in]

Type: <b>ULONG</b>

Source <b>ULONG</b> value.


### -param ppropvar [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a VT_UI4 propvariant.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/en-us/library/Bb762311(v=VS.85).aspx">InitPropVariantFromUInt32</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromUInt32(56, &amp;propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_UI4.
    PropVariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb762340(v=VS.85).aspx">InitVariantFromUInt32</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776569(v=VS.85).aspx">PropVariantToUInt32</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776572(v=VS.85).aspx">PropVariantToUInt32WithDefault</a>
 

 

