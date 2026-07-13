---
UID: NF:propvarutil.InitVariantFromResource
title: InitVariantFromResource function (propvarutil.h)
description: Initializes a VARIANT structure based on a string resource embedded in an executable file.
helpviewer_keywords: ["InitVariantFromResource","InitVariantFromResource function [Windows Properties]","_shell_InitVariantFromResource","properties.InitVariantFromResource","propvarutil/InitVariantFromResource","shell.InitVariantFromResource"]
old-location: properties\InitVariantFromResource.htm
tech.root: properties
ms.assetid: ae309a04-7b21-46ef-b481-2593dc162e19
ms.date: 12/05/2018
ms.keywords: InitVariantFromResource, InitVariantFromResource function [Windows Properties], _shell_InitVariantFromResource, properties.InitVariantFromResource, propvarutil/InitVariantFromResource, shell.InitVariantFromResource
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
 - InitVariantFromResource
 - propvarutil/InitVariantFromResource
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
 - InitVariantFromResource
---

# InitVariantFromResource function


## -description

Initializes a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure based on a string resource embedded in an executable file.

## -parameters

### -param hinst [in]

Type: <b>HINSTANCE</b>

Handle to an instance of the module whose executable file contains the string resource.

### -param id [in]

Type: <b>UINT</b>

Integer identifier of the string to be loaded.

### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Creates a VT_BSTR variant. If the resource does not exist, this function initializes the VARIANT as VT_EMPTY and returns a failure code.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromresource">InitVariantFromResource</a>.


```cpp
// HINSTANCE hinst;
// UINT id;
// Assume variables hinst and id are initialized and valid.
VARIANT var;

HRESULT hr = InitVariantFromResource(hinst, id, &var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_BSTR.
    VariantClear(&var);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromresource">InitPropVariantFromResource</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromstring">InitVariantFromString</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadstringa">LoadString</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttostring">VariantToString</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttostringwithdefault">VariantToStringWithDefault</a>