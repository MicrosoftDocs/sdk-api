---
UID: NF:propvarutil.InitVariantFromUInt32
title: InitVariantFromUInt32 function
author: windows-sdk-content
description: Initializes a VARIANT structure with an unsigned 32-bit integer value.
old-location: properties\InitVariantFromUInt32.htm
tech.root: properties
ms.assetid: df260524-188d-4c2a-8996-ce22ddda41e7
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: InitVariantFromUInt32, InitVariantFromUInt32 function [Windows Properties], _shell_InitVariantFromUInt32, properties.InitVariantFromUInt32, propvarutil/InitVariantFromUInt32, shell.InitVariantFromUInt32
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
 - InitVariantFromUInt32
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
- apiref
: 
- 
: 
- InitVariantFromUInt32
: 
---

# InitVariantFromUInt32 function


## -description


Initializes a <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> structure with an unsigned 32-bit integer value.


## -parameters




### -param ulVal [in]

Type: <b>ULONG</b>

Source <b>ULONG</b> value.


### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a VT_UI4 variant.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/en-us/library/Bb762340(v=VS.85).aspx">InitVariantFromUInt32</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VARIANT var;

HRESULT hr = InitVariantFromUInt32(3, &amp;var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_UI4.
 
    VariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb762311(v=VS.85).aspx">InitPropVariantFromUInt32</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776627(v=VS.85).aspx">VariantToUInt32</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776630(v=VS.85).aspx">VariantToUInt32WithDefault</a>
 

 

