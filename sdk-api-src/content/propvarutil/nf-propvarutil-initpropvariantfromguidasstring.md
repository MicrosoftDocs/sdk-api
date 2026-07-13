---
UID: NF:propvarutil.InitPropVariantFromGUIDAsString
title: InitPropVariantFromGUIDAsString function (propvarutil.h)
description: Initializes a PROPVARIANT structure based on a GUID. The structure is initialized as VT_LPWSTR.
helpviewer_keywords: ["InitPropVariantFromGUIDAsString","InitPropVariantFromGUIDAsString function [Windows Properties]","properties.InitPropVariantFromGUIDAsString","propvarutil/InitPropVariantFromGUIDAsString","shell.InitPropVariantFromGUIDAsString","shell_InitPropVariantFromGUIDAsString"]
old-location: properties\InitPropVariantFromGUIDAsString.htm
tech.root: properties
ms.assetid: bcc343f7-741f-4cdd-bd2f-ae4786faab0e
ms.date: 12/05/2018
ms.keywords: InitPropVariantFromGUIDAsString, InitPropVariantFromGUIDAsString function [Windows Properties], properties.InitPropVariantFromGUIDAsString, propvarutil/InitPropVariantFromGUIDAsString, shell.InitPropVariantFromGUIDAsString, shell_InitPropVariantFromGUIDAsString
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
 - InitPropVariantFromGUIDAsString
 - propvarutil/InitPropVariantFromGUIDAsString
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
 - InitPropVariantFromGUIDAsString
---

# InitPropVariantFromGUIDAsString function


## -description

Initializes a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure based on a <b>GUID</b>. The structure is initialized as VT_LPWSTR.

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

Creates a VT_LPWSTR <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>, which formats the GUID in a form similar to <code>{c200e360-38c5-11ce-ae62-08002b2b79ef}</code>.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <b>InitPropVariantFromGUIDAsString</b>.


```cpp
PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromGUIDAsString(FMTID_DocSummaryInformation, &propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_LPWSTR.
 
    PropVariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromclsid">InitPropVariantFromCLSID</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromguidasbuffer">InitPropVariantFromGUIDAsBuffer</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromguidasstring">InitVariantFromGUIDAsString</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostring">PropVariantToString</a>