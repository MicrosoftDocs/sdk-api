---
UID: NF:propvarutil.InitVariantFromStrRet
title: InitVariantFromStrRet function
author: windows-sdk-content
description: Initializes a VARIANT structure with a string stored in a STRRET structure.
old-location: properties\InitVariantFromStrRet.htm
tech.root: properties
ms.assetid: 8e9542a9-9ed0-4e44-b9b1-32b31151bd8e
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: InitVariantFromStrRet, InitVariantFromStrRet function [Windows Properties], _shell_InitVariantFromStrRet, properties.InitVariantFromStrRet, propvarutil/InitVariantFromStrRet, shell.InitVariantFromStrRet
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
 - InitVariantFromStrRet
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
- apiref
: 
- 
: 
- InitVariantFromStrRet
: 
---

# InitVariantFromStrRet function


## -description


Initializes a <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> structure with a string stored in a <a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a> structure.


## -parameters




### -param pstrret [in]

Type: <b><a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a> structure.


### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

PIDL of the item whose details are being retrieved.


### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a VT_BSTR variant.

<div class="alert"><b>Note</b>  This function frees the resources used for the <a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a> contents.</div>
<div> </div>

#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.InitVariantFromStrRet">InitVariantFromStrRet</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// STRRET strret;
// PCUITEMID_CHILD pidl;
// Assume variables strret and pidl are initialized and valid.
VARIANT var;

HRESULT hr = InitVariantFromStrRet(strret, pidl, &amp;var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_BSTR.
    VariantClear(&amp;var);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitVariantFromString">InitVariantFromString</a>



<a href="shell.VariantToString">VariantToString</a>



<a href="shell.VariantToStringWithDefault">VariantToStringWithDefault</a>
 

 

