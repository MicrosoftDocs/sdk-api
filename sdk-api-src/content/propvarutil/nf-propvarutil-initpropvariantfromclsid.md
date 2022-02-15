---
UID: NF:propvarutil.InitPropVariantFromCLSID
title: InitPropVariantFromCLSID function (propvarutil.h)
description: Initializes a PROPVARIANT structure based on a class identifier (CLSID).
helpviewer_keywords: ["InitPropVariantFromCLSID","InitPropVariantFromCLSID function [Windows Properties]","properties.InitPropVariantFromCLSID","propvarutil/InitPropVariantFromCLSID","shell.InitPropVariantFromCLSID","shell_InitPropVariantFromCLSID"]
old-location: properties\InitPropVariantFromCLSID.htm
tech.root: properties
ms.assetid: a48a8927-2718-4f9c-96f2-ab370206550b
ms.date: 12/05/2018
ms.keywords: InitPropVariantFromCLSID, InitPropVariantFromCLSID function [Windows Properties], properties.InitPropVariantFromCLSID, propvarutil/InitPropVariantFromCLSID, shell.InitPropVariantFromCLSID, shell_InitPropVariantFromCLSID
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
 - InitPropVariantFromCLSID
 - propvarutil/InitPropVariantFromCLSID
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
 - InitPropVariantFromCLSID
---

# InitPropVariantFromCLSID function


## -description

Initializes a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure based on a class identifier (CLSID).

## -parameters

### -param clsid [in]

Type: <b>REFCLSID</b>

Reference to the CLSID.

### -param ppropvar [out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Creates a VT_CLSID propvariant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromclsid">InitPropVariantFromCLSID</a>.


```cpp
PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromCLSID(CLSID_PropertySystem, &propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_CLSID.
 
    PropVariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromguidasbuffer">InitVariantFromGUIDAsBuffer</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromguidasstring">InitVariantFromGUIDAsString</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoclsid">PropVariantToCLSID</a>