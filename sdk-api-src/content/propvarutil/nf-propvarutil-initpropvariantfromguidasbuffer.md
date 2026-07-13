---
UID: NF:propvarutil.InitPropVariantFromGUIDAsBuffer
title: InitPropVariantFromGUIDAsBuffer function (propvarutil.h)
description: Initializes a PROPVARIANT structure based on a GUID. The structure is initialized as VT_VECTOR | VT_UI1.
helpviewer_keywords: ["InitPropVariantFromGUIDAsBuffer","InitPropVariantFromGUIDAsBuffer function [Windows Properties]","properties.InitPropVariantFromGUIDAsBuffer","propvarutil/InitPropVariantFromGUIDAsBuffer","shell.InitPropVariantFromGUIDAsBuffer","shell_InitPropVariantFromGUIDAsBuffer"]
old-location: properties\InitPropVariantFromGUIDAsBuffer.htm
tech.root: properties
ms.assetid: 9ff3ec09-3314-4830-b970-b33f5a53d66c
ms.date: 12/05/2018
ms.keywords: InitPropVariantFromGUIDAsBuffer, InitPropVariantFromGUIDAsBuffer function [Windows Properties], properties.InitPropVariantFromGUIDAsBuffer, propvarutil/InitPropVariantFromGUIDAsBuffer, shell.InitPropVariantFromGUIDAsBuffer, shell_InitPropVariantFromGUIDAsBuffer
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
 - InitPropVariantFromGUIDAsBuffer
 - propvarutil/InitPropVariantFromGUIDAsBuffer
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
 - InitPropVariantFromGUIDAsBuffer
---

# InitPropVariantFromGUIDAsBuffer function


## -description

Initializes a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure based on a <b>GUID</b>. The structure is initialized as VT_VECTOR | VT_UI1.

## -parameters

### -param guid [in]

Type: <b>REFGUID</b>

Reference to the source <b>GUID</b>.

### -param ppropvar [out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Creates a VT_VECTOR | VT_UI1 propvariant.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <b>InitPropVariantFromGUIDAsBuffer</b>.


```cpp
PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromGUIDAsBuffer(FMTID_DocSummaryInformation, &propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_VECTOR | VT_UI1.
 
    PropVariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromclsid">InitPropVariantFromCLSID</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromguidasstring">InitPropVariantFromGUIDAsString</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromguidasbuffer">InitVariantFromGUIDAsBuffer</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttobuffer">PropVariantToBuffer</a>