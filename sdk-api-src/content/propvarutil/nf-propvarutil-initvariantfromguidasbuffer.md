---
UID: NF:propvarutil.InitVariantFromGUIDAsBuffer
title: InitVariantFromGUIDAsBuffer function (propvarutil.h)
description: Initializes a VARIANT structure based on a GUID. The structure is initialized as VT_ARRAY | VT_UI1.
helpviewer_keywords: ["InitVariantFromGUIDAsBuffer","InitVariantFromGUIDAsBuffer function [Windows Properties]","properties.InitVariantFromGUIDAsBuffer","propvarutil/InitVariantFromGUIDAsBuffer","shell.InitVariantFromGUIDAsBuffer","shell_InitVariantFromGUIDAsBuffer"]
old-location: properties\InitVariantFromGUIDAsBuffer.htm
tech.root: properties
ms.assetid: c46c1263-527a-4a64-b4c9-4c4779b271c7
ms.date: 12/05/2018
ms.keywords: InitVariantFromGUIDAsBuffer, InitVariantFromGUIDAsBuffer function [Windows Properties], properties.InitVariantFromGUIDAsBuffer, propvarutil/InitVariantFromGUIDAsBuffer, shell.InitVariantFromGUIDAsBuffer, shell_InitVariantFromGUIDAsBuffer
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
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - InitVariantFromGUIDAsBuffer
 - propvarutil/InitVariantFromGUIDAsBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Propvarutil.h
api_name:
 - InitVariantFromGUIDAsBuffer
---

# InitVariantFromGUIDAsBuffer function


## -description

Initializes a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure based on a <b>GUID</b>. The structure is initialized as VT_ARRAY | VT_UI1.

## -parameters

### -param guid [in]

Type: <b>REFGUID</b>

Reference to the source <b>GUID</b>.

### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromguidasbuffer">InitVariantFromGUIDAsBuffer</a>.


```cpp
VARIANT var;

HRESULT hr = InitVariantFromGUIDAsBuffer(FMTID_DocSummaryInformation, &var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_ARRAY | VT_UI1.
    VariantClear(&var);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromclsid">InitPropVariantFromCLSID</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromguidasstring">InitVariantFromGUIDAsString</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttobuffer">VariantToBuffer</a>