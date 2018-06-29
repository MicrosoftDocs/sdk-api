---
UID: NF:propvarutil.InitVariantFromBuffer
title: InitVariantFromBuffer function
author: windows-sdk-content
description: Initializes a VARIANT structure with the contents of a buffer.
old-location: properties\InitVariantFromBuffer.htm
old-project: properties
ms.assetid: 4dd28a13-2161-4258-a32f-57e5bd8ce091
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: InitVariantFromBuffer, InitVariantFromBuffer function [Windows Properties], _shell_InitVariantFromBuffer, properties.InitVariantFromBuffer, propvarutil/InitVariantFromBuffer, shell.InitVariantFromBuffer
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
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - InitVariantFromBuffer
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: ADAM
---

# InitVariantFromBuffer function


## -description


Initializes a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure with the contents of a buffer.


## -parameters




### -param pv [in]

Type: <b>const VOID*</b>

Pointer to the source buffer.


### -param cb [in]

Type: <b>UINT</b>

The length of the buffer, in bytes.


### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a VT_ARRAY | VT_UI1 variant..


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/library/Bb762318(v=VS.85).aspx">InitVariantFromBuffer</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// void *pv;
// UINT cb;
// Assume variable pv and cb are initialized and valid. pv points to a 
// buffer and cb contains the size of the buffer in bytes.
VARIANT var;

HRESULT hr = InitVariantFromBuffer(pv, cb, &amp; var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_ARRAY | VT_UI1.
    VariantClear(&amp;var);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/Bb762289(v=VS.85).aspx">InitPropVariantFromBuffer</a>



<a href="https://msdn.microsoft.com/library/Bb776596(v=VS.85).aspx">VariantToBuffer</a>
 

 

