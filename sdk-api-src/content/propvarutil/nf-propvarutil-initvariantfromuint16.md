---
UID: NF:propvarutil.InitVariantFromUInt16
title: InitVariantFromUInt16 function
author: windows-sdk-content
description: Initializes a VARIANT structure with an unsigned 16-bit integer value.
old-location: properties\InitVariantFromUInt16.htm
old-project: properties
ms.assetid: ec919626-6af3-4e33-85a5-134274220c67
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: InitVariantFromUInt16, InitVariantFromUInt16 function [Windows Properties], _shell_InitVariantFromUInt16, properties.InitVariantFromUInt16, propvarutil/InitVariantFromUInt16, shell.InitVariantFromUInt16
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
 - InitVariantFromUInt16
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# InitVariantFromUInt16 function


## -description


Initializes a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure with an unsigned 16-bit integer value.


## -parameters




### -param uiVal [in]

Type: <b>USHORT</b>

Source <b>USHORT</b> value.


### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a VT_UI2 variant.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/library/Bb762338(v=VS.85).aspx">InitVariantFromUInt16</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VARIANT var;

HRESULT hr = InitVariantFromUInt16(3, &amp;var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_UI2.
    VariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/Bb762309(v=VS.85).aspx">InitPropVariantFromUInt16</a>



<a href="https://msdn.microsoft.com/library/Bb776623(v=VS.85).aspx">VariantToUInt16</a>



<a href="https://msdn.microsoft.com/library/Bb776626(v=VS.85).aspx">VariantToUInt16WithDefault</a>
 

 

