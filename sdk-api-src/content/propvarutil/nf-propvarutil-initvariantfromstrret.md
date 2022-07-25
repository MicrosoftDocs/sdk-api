---
UID: NF:propvarutil.InitVariantFromStrRet
title: InitVariantFromStrRet function (propvarutil.h)
description: Initializes a VARIANT structure with a string stored in a STRRET structure.
helpviewer_keywords: ["InitVariantFromStrRet","InitVariantFromStrRet function [Windows Properties]","_shell_InitVariantFromStrRet","properties.InitVariantFromStrRet","propvarutil/InitVariantFromStrRet","shell.InitVariantFromStrRet"]
old-location: properties\InitVariantFromStrRet.htm
tech.root: properties
ms.assetid: 8e9542a9-9ed0-4e44-b9b1-32b31151bd8e
ms.date: 12/05/2018
ms.keywords: InitVariantFromStrRet, InitVariantFromStrRet function [Windows Properties], _shell_InitVariantFromStrRet, properties.InitVariantFromStrRet, propvarutil/InitVariantFromStrRet, shell.InitVariantFromStrRet
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
 - InitVariantFromStrRet
 - propvarutil/InitVariantFromStrRet
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
 - InitVariantFromStrRet
---

# InitVariantFromStrRet function


## -description

Initializes a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure with a string stored in a <a href="/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a> structure.

## -parameters

### -param pstrret [in]

Type: <b><a href="/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a>*</b>

Pointer to a <a href="/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a> structure.

### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

PIDL of the item whose details are being retrieved.

### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Creates a VT_BSTR variant.

<div class="alert"><b>Note</b>  This function frees the resources used for the <a href="/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a> contents.</div>
<div> </div>

#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromstrret">InitVariantFromStrRet</a>.


```cpp
// STRRET strret;
// PCUITEMID_CHILD pidl;
// Assume variables strret and pidl are initialized and valid.
VARIANT var;

HRESULT hr = InitVariantFromStrRet(strret, pidl, &var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_BSTR.
    VariantClear(&var);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromstring">InitVariantFromString</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttostring">VariantToString</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttostringwithdefault">VariantToStringWithDefault</a>