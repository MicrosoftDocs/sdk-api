---
UID: NF:propvarutil.InitVariantFromVariantArrayElem
title: InitVariantFromVariantArrayElem function (propvarutil.h)
description: Initializes a VARIANT structure with a value stored in another VARIANT structure.
helpviewer_keywords: ["InitVariantFromVariantArrayElem","InitVariantFromVariantArrayElem function [Windows Properties]","_shell_InitVariantFromVariantArrayElem","properties.InitVariantFromVariantArrayElem","propvarutil/InitVariantFromVariantArrayElem","shell.InitVariantFromVariantArrayElem"]
old-location: properties\InitVariantFromVariantArrayElem.htm
tech.root: properties
ms.assetid: 531731a5-7a13-49be-8512-5cf25c96ee35
ms.date: 12/05/2018
ms.keywords: InitVariantFromVariantArrayElem, InitVariantFromVariantArrayElem function [Windows Properties], _shell_InitVariantFromVariantArrayElem, properties.InitVariantFromVariantArrayElem, propvarutil/InitVariantFromVariantArrayElem, shell.InitVariantFromVariantArrayElem
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
 - InitVariantFromVariantArrayElem
 - propvarutil/InitVariantFromVariantArrayElem
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
 - InitVariantFromVariantArrayElem
---

# InitVariantFromVariantArrayElem function


## -description

Initializes a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure with a value stored in another <b>VARIANT</b> structure.

## -parameters

### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to the source <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure.

### -param iElem [in]

Type: <b>ULONG</b>

Index of one of the source <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure elements.

### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This helper function works for <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structures of the following types:
                
                

<ul>
<li>VT_BSTR</li>
<li>VT_BOOL</li>
<li>VT_I2</li>
<li>VT_I4</li>
<li>VT_I8</li>
<li>VT_U12</li>
<li>VT_U14</li>
<li>VT_U18</li>
<li>VT_DATE</li>
<li>VT_ARRAY | (any one of VT_BSTR, VT_BOOL, VT_I2, VT_I4, VT_I8, VT_U12, VT_U14, VT_U18, VT_DATE)</li>
</ul>
Additional types may be supported in the future.

This function extracts a single value from the source <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure and uses that value to initialize the output <b>VARIANT</b> structure. The calling application must use <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear">VariantClear</a> to free the <b>VARIANT</b> referred to by <i>pvar</i> when it is no longer needed.

If the source <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> is an array, <i>iElem</i> must be less than the number of elements in the array.

If the source <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> has a single value, <i>iElem</i> must be 0.

If the source <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> is empty, this function always returns an error code.

You can use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-variantgetelementcount">VariantGetElementCount</a> to obtain the number of elements in the array or array.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromvariantarrayelem">InitVariantFromVariantArrayElem</a> in an iteration statement to access the values in a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a>.


```cpp
// VARIANT var;
// Assume var is initialized and valid.
UINT cElem = VariantGetElementCount(var);
HRESULT hr = <mark type="const">S_OK</mark>;

for (UINT iElem = 0; SUCCEEDED(hr) && iElem < cElem; iElem ++)
{
    VARIANT varElem = {0};

    hr = InitVariantFromVariantArrayElem(var, iElem, &varElem);

    if (SUCCEEDED(hr))
    {
        // varElem is now valid.
        VariantClear(&varElem);
    }
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfrompropvariantvectorelem">InitPropVariantFromPropVariantVectorElem</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-variantgetelem">VariantGetElem</a>