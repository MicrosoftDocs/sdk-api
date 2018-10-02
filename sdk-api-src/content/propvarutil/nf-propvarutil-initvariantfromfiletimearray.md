---
UID: NF:propvarutil.InitVariantFromFileTimeArray
title: InitVariantFromFileTimeArray function
author: windows-sdk-content
description: Initializes a VARIANT structure with an array of FILETIME structures.
old-location: properties\InitVariantFromFileTimeArray.htm
tech.root: properties
ms.assetid: d1b25aec-f302-4d39-93c1-0fcb2d7dbf45
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: InitVariantFromFileTimeArray, InitVariantFromFileTimeArray function [Windows Properties], _shell_InitVariantFromFileTimeArray, properties.InitVariantFromFileTimeArray, propvarutil/InitVariantFromFileTimeArray, shell.InitVariantFromFileTimeArray
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
req.lib: Propsys.lib
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
 - InitVariantFromFileTimeArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# InitVariantFromFileTimeArray function


## -description


Initializes a <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> structure with an array of <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structures.


## -parameters




### -param prgft [in]

Type: <b>const FILETIME*</b>

Pointer to an array of <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structures.


### -param cElems [in]

Type: <b>ULONG</b>

The number of elements in the array pointed to by <i>prgft</i>.


### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a VT_ARRAY | VT_DATE variant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.InitVariantFromFileTimeArray">InitVariantFromFileTimeArray</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// FILETIME rgFileTimes[3];
// Assume variable rgFileTimes is initialized and valid.
VARIANT var;

HRESULT hr = InitVariantFromFileTimeArray(rgFileTimes, ARRAYSIZE(rgFileTimes), &amp;var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_ARRAY | VT_DATE.
    VariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitPropVariantFromFileTimeVector">InitPropVariantFromFileTimeVector</a>
 

 

