---
UID: NF:propvarutil.PropVariantToCLSID
title: PropVariantToCLSID function (propvarutil.h)
description: Extracts class identifier (CLSID) property value of a PROPVARIANT structure.
helpviewer_keywords: ["PropVariantToCLSID","PropVariantToCLSID function [Windows Properties]","_shell_PropVariantToCLSID","properties.PropVariantToCLSID","propvarutil/PropVariantToCLSID","shell.PropVariantToCLSID"]
old-location: properties\PropVariantToCLSID.htm
tech.root: properties
ms.assetid: 35b638e3-7610-49d6-92f3-5e4021fea635
ms.date: 12/05/2018
ms.keywords: PropVariantToCLSID, PropVariantToCLSID function [Windows Properties], _shell_PropVariantToCLSID, properties.PropVariantToCLSID, propvarutil/PropVariantToCLSID, shell.PropVariantToCLSID
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
 - PropVariantToCLSID
 - propvarutil/PropVariantToCLSID
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
 - PropVariantToCLSID
---

# PropVariantToCLSID function


## -description

Extracts class identifier (CLSID) property value of a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -parameters

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param pclsid [out]

Type: <b>CLSID*</b>

When this function returns, contains the extracted property value if one exists.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This helper function works for<a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structures of the following types:             

                

<ul>
<li>VT_CLSID</li>
<li>VT_BSTR</li>
<li>VT_LPWSTR</li>
<li>VT_ARRAY | VT_UI1</li>
</ul>
This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoclsid">PropVariantToCLSID</a> is used in places where the calling application expects a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> to hold a single CLSID or GUID value. For instance, an application obtaining values from a property store can use this to safely extract the CLSID value for GUID properties.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoclsid">PropVariantToCLSID</a> to access a CLSID value in a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>.


```cpp
// IPropertyStore *ppropstore;
// Assume variable ppropstore is initialized and valid
PROPVARIANT propvar = {0};

HRESULT hr = ppropstore->GetValue(PKEY_Sync_HandlerCollectionID, &propvar);
if (SUCCEEDED(hr))
{
        // PKEY_Sync_HandlerCollectionID is expected to produce a VT_CLSID or VT_EMPTY value.
        // PropVariantToCLSID will convert VT_EMPTY to a failure code.
        CLSID clsidCollectionID;

        hr = PropVariantToCLSID(propvar, &clsidCollectionID);
        if (SUCCEEDED(hr))
        {
             // clsidCollectionID is now valid
        }
        else
        {
            // the extraction failed
        }
        PropVariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromclsid">InitPropVariantFromCLSID</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoguid">PropVariantToGUID</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttoguid">VariantToGUID</a>