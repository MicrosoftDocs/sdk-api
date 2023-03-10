---
UID: NF:propvarutil.InitVariantFromFileTime
title: InitVariantFromFileTime function (propvarutil.h)
description: Initializes a VARIANT structure with the contents of a FILETIME structure.
helpviewer_keywords: ["InitVariantFromFileTime","InitVariantFromFileTime function [Windows Properties]","_shell_InitVariantFromFileTime","properties.InitVariantFromFileTime","propvarutil/InitVariantFromFileTime","shell.InitVariantFromFileTime"]
old-location: properties\InitVariantFromFileTime.htm
tech.root: properties
ms.assetid: cd61a268-ef73-4dd3-98d4-9811922d01f4
ms.date: 12/05/2018
ms.keywords: InitVariantFromFileTime, InitVariantFromFileTime function [Windows Properties], _shell_InitVariantFromFileTime, properties.InitVariantFromFileTime, propvarutil/InitVariantFromFileTime, shell.InitVariantFromFileTime
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
 - InitVariantFromFileTime
 - propvarutil/InitVariantFromFileTime
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
 - InitVariantFromFileTime
---

# InitVariantFromFileTime function


## -description

Initializes a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure with the contents of a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure.

## -parameters

### -param pft [in]

Type: <b>const FILETIME*</b>

Pointer to date and time information stored in a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure.

### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Creates a VT_DATE variant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromfiletime">InitVariantFromFileTime</a>.


```cpp
VARIANT var;
FILETIME ft;

GetSystemTimeAsFileTime(&ft);

HRESULT hr = InitVariantFromFileTime(&ft, &var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_DATE.
    VariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime">GetSystemTimeAsFileTime</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromfiletime">InitPropVariantFromFileTime</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttofiletime">VariantToFileTime</a>