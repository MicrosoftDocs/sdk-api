---
UID: NF:propvarutil.InitVariantFromGUIDAsString
title: InitVariantFromGUIDAsString function (propvarutil.h)
description: Initializes a VARIANT structure based on a GUID. The structure is initialized as a VT_BSTR type.
helpviewer_keywords: ["InitVariantFromGUIDAsString","InitVariantFromGUIDAsString function [Windows Shell]","_shell_InitVariantFromGUIDAsString","properties.InitVariantFromGUIDAsString","propvarutil/InitVariantFromGUIDAsString"]
old-location: properties\InitVariantFromGUIDAsString.htm
tech.root: properties
ms.assetid: 2a78257a-a8ce-45e8-aea2-dfa9f380528a
ms.date: 12/05/2018
ms.keywords: InitVariantFromGUIDAsString, InitVariantFromGUIDAsString function [Windows Shell], _shell_InitVariantFromGUIDAsString, properties.InitVariantFromGUIDAsString, propvarutil/InitVariantFromGUIDAsString
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
 - InitVariantFromGUIDAsString
 - propvarutil/InitVariantFromGUIDAsString
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
 - InitVariantFromGUIDAsString
---

# InitVariantFromGUIDAsString function


## -description

Initializes a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure based on a <b>GUID</b>. The structure is initialized as a <b>VT_BSTR</b> type.

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

Creates a VT_BSTR variant, formatting the GUID in a form similar to <code>{c200e360-38c5-11ce-ae62-08002b2b79ef}</code>.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <b>InitVariantFromGUIDAsString</b>.


```cpp
VARIANT var;

HRESULT hr = InitVariantFromGUIDAsString(FMTID_DocSummaryInformation, &var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_BSTR.
    VariantClear(&var);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromclsid">InitPropVariantFromCLSID</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromguidasbuffer">InitVariantFromGUIDAsBuffer</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttoguid">VariantToGUID</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttostring">VariantToString</a>