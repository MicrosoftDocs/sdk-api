---
UID: NF:propvarutil.PropVariantGetFileTimeElem
title: PropVariantGetFileTimeElem function (propvarutil.h)
description: Extracts a single FILETIME element from a PROPVARIANT structure of type VT_FILETIME, VT_VECTOR | VT_FILETIME, or VT_ARRAY | VT_FILETIME.
helpviewer_keywords: ["PropVariantGetFileTimeElem","PropVariantGetFileTimeElem function [Windows Properties]","_shell_PropVariantGetFileTimeElem","properties.PropVariantGetFileTimeElem","propvarutil/PropVariantGetFileTimeElem","shell.PropVariantGetFileTimeElem"]
old-location: properties\PropVariantGetFileTimeElem.htm
tech.root: properties
ms.assetid: e38b16ed-84cb-4444-bfbd-1165595bc9b5
ms.date: 12/05/2018
ms.keywords: PropVariantGetFileTimeElem, PropVariantGetFileTimeElem function [Windows Properties], _shell_PropVariantGetFileTimeElem, properties.PropVariantGetFileTimeElem, propvarutil/PropVariantGetFileTimeElem, shell.PropVariantGetFileTimeElem
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
 - PropVariantGetFileTimeElem
 - propvarutil/PropVariantGetFileTimeElem
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
 - PropVariantGetFileTimeElem
---

# PropVariantGetFileTimeElem function


## -description

Extracts a single <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> element from a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure of type VT_FILETIME, VT_VECTOR | VT_FILETIME, or VT_ARRAY | VT_FILETIME.

## -parameters

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

The source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param iElem [in]

Type: <b>ULONG</b>

Specifies vector or array index; otherwise, this value must be 0.

### -param pftVal [out]

Type: <b>FILETIME*</b>

When this function returns, contains the extracted filetime value.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type VT_FILETIME, <i>iElem</i> must be 0; otherwise, <i>iElem</i> must be less than the number of elements in the vector or array. You can use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetelementcount">PropVariantGetElementCount</a> to obtain the number of elements in the vector or array.


#### Examples

The following code example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetfiletimeelem">PropVariantGetFileTimeElem</a> in an iteration statement to access the values in <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>.
      
                


```cpp
// PROPVARIANT propvar;
// Assume propvar is initialized and valid;

if ((propvar.vt & VT_TYPEMASK) == VT_FILETIME)
{
    UINT cElem = PropVariantGetElementCount(propvar);
    HRESULT hr = <mark type="const">S_OK</mark>;

    for (UINT iElem = 0; SUCCEEDED(hr) && iElem < cElem; iElem ++)
    {
        FILETIME ftValue;
        hr = PropVariantGetFileTimeElem(propvar, iElem, &ftValue);

        if (SUCCEEDED(hr))
        {
            // ftValue is valid now
        }
    }
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetelem">PropVariantGetElem</a>