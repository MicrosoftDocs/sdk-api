---
UID: NF:propvarutil.InitVariantFromFileTime
title: InitVariantFromFileTime function
author: windows-sdk-content
description: Initializes a VARIANT structure with the contents of a FILETIME structure.
old-location: properties\InitVariantFromFileTime.htm
tech.root: properties
ms.assetid: cd61a268-ef73-4dd3-98d4-9811922d01f4
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: InitVariantFromFileTime, InitVariantFromFileTime function [Windows Properties], _shell_InitVariantFromFileTime, properties.InitVariantFromFileTime, propvarutil/InitVariantFromFileTime, shell.InitVariantFromFileTime
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
 - InitVariantFromFileTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
- apiref
: 
- 
: 
- InitVariantFromFileTime
: 
---

# InitVariantFromFileTime function


## -description


Initializes a <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> structure with the contents of a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure.


## -parameters




### -param pft [in]

Type: <b>const FILETIME*</b>

Pointer to date and time information stored in a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure.


### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a VT_DATE variant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/en-us/library/Bb762323(v=VS.85).aspx">InitVariantFromFileTime</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VARIANT var;
FILETIME ft;

GetSystemTimeAsFileTime(&amp;ft);

HRESULT hr = InitVariantFromFileTime(&amp;ft, &amp;var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_DATE.
    VariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/adf7ff5d-2d30-4490-9868-9ad78ef7a0b6">GetSystemTimeAsFileTime</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb762293(v=VS.85).aspx">InitPropVariantFromFileTime</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776602(v=VS.85).aspx">VariantToFileTime</a>
 

 

