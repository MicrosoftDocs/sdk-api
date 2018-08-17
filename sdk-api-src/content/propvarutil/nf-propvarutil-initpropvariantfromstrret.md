---
UID: NF:propvarutil.InitPropVariantFromStrRet
title: InitPropVariantFromStrRet function
author: windows-sdk-content
description: Initializes a PROPVARIANT structure based on a string stored in a STRRET structure.
old-location: properties\InitPropVariantFromStrRet.htm
old-project: properties
ms.assetid: 5c02e2ee-14c2-4966-83e7-16dfbf81b879
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: InitPropVariantFromStrRet, InitPropVariantFromStrRet function [Windows Properties], properties.InitPropVariantFromStrRet, propvarutil/InitPropVariantFromStrRet, shell.InitPropVariantFromStrRet, shell_InitPropVariantFromStrRet
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: propvarutil.h
req.include-header: 
req.redist: Windows Desktop Search (WDS) 3.0
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
 - InitPropVariantFromStrRet
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: ADAM
---

# InitPropVariantFromStrRet function


## -description


Initializes a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure based on a string stored in a <a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a> structure.


## -parameters




### -param pstrret [in, out]

Type: <b><a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a> structure that contains the string.


### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

PIDL of the item whose details are being retrieved.


### -param ppropvar [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a VT_LPWSTR propvariant.

<div class="alert"><b>Note</b>  This function frees the memory used for the <a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a> contents.</div>
<div> </div>

#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.InitPropVariantFromStrRet">InitPropVariantFromStrRet</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// STRRET strret;
// PCUITEMID_CHILD pidl;
// Assume variables strret and pidl are initialized and valid.
PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromStrRet(strret, pidl, &amp;propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_LPWSTR.
    PropVariantClear(&amp;propvar);
    
    // Any allocated memory associated with strret has been freed.
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitPropVariantFromString">InitPropVariantFromString</a>



<a href="shell.InitVariantFromStrRet">InitVariantFromStrRet</a>



<a href="shell.PropVariantToString">PropVariantToString</a>



<a href="shell.PropVariantToStringWithDefault">PropVariantToStringWithDefault</a>
 

 

