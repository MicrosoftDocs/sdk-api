---
UID: NF:propvarutil.InitPropVariantFromStrRet
title: InitPropVariantFromStrRet function (propvarutil.h)
description: Initializes a PROPVARIANT structure based on a string stored in a STRRET structure.
helpviewer_keywords: ["InitPropVariantFromStrRet","InitPropVariantFromStrRet function [Windows Properties]","properties.InitPropVariantFromStrRet","propvarutil/InitPropVariantFromStrRet","shell.InitPropVariantFromStrRet","shell_InitPropVariantFromStrRet"]
old-location: properties\InitPropVariantFromStrRet.htm
tech.root: properties
ms.assetid: 5c02e2ee-14c2-4966-83e7-16dfbf81b879
ms.date: 12/05/2018
ms.keywords: InitPropVariantFromStrRet, InitPropVariantFromStrRet function [Windows Properties], properties.InitPropVariantFromStrRet, propvarutil/InitPropVariantFromStrRet, shell.InitPropVariantFromStrRet, shell_InitPropVariantFromStrRet
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
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - InitPropVariantFromStrRet
 - propvarutil/InitPropVariantFromStrRet
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - InitPropVariantFromStrRet
---

# InitPropVariantFromStrRet function


## -description

Initializes a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure based on a string stored in a <a href="/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a> structure.

## -parameters

### -param pstrret [in, out]

Type: <b><a href="/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a>*</b>

Pointer to a <a href="/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a> structure that contains the string.

### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

PIDL of the item whose details are being retrieved.

### -param ppropvar [out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Creates a VT_LPWSTR propvariant.

<div class="alert"><b>Note</b>  This function frees the memory used for the <a href="/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a> contents.</div>
<div> </div>

#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromstrret">InitPropVariantFromStrRet</a>.


```cpp
// STRRET strret;
// PCUITEMID_CHILD pidl;
// Assume variables strret and pidl are initialized and valid.
PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromStrRet(strret, pidl, &propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_LPWSTR.
    PropVariantClear(&propvar);
    
    // Any allocated memory associated with strret has been freed.
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromstring">InitPropVariantFromString</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromstrret">InitVariantFromStrRet</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostring">PropVariantToString</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostringwithdefault">PropVariantToStringWithDefault</a>