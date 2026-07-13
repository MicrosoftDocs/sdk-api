---
UID: NF:propvarutil.PropVariantToFileTime
title: PropVariantToFileTime function (propvarutil.h)
description: Extracts the FILETIME structure from a PROPVARIANT structure.
helpviewer_keywords: ["PSTF_LOCAL","PSTF_UTC","PropVariantToFileTime","PropVariantToFileTime function [Windows Properties]","_shell_PropVariantToFileTime","properties.PropVariantToFileTime","propvarutil/PropVariantToFileTime","shell.PropVariantToFileTime"]
old-location: properties\PropVariantToFileTime.htm
tech.root: properties
ms.assetid: fc835395-8c2c-4f6a-88be-f438625442b9
ms.date: 12/05/2018
ms.keywords: PSTF_LOCAL, PSTF_UTC, PropVariantToFileTime, PropVariantToFileTime function [Windows Properties], _shell_PropVariantToFileTime, properties.PropVariantToFileTime, propvarutil/PropVariantToFileTime, shell.PropVariantToFileTime
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
 - PropVariantToFileTime
 - propvarutil/PropVariantToFileTime
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
 - PropVariantToFileTime
---

# PropVariantToFileTime function


## -description

Extracts the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure from a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -parameters

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param pstfOut [in]

Type: <b>PSTIME_FLAGS</b>

Specifies one of the following time flags.



#### PSTF_UTC (0)

Indicates the output will use coordinated universal time.



#### PSTF_LOCAL (1)

Indicates the output will use local time.

### -param pftOut [out]

Type: <b>FILETIME*</b>

When this function returns, contains the extracted <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This helper function is used in places where the calling application expects a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> to hold a single filetime value. For instance, an application obtaining values from a property store can use this to safely extract a filetime value for filetime properties.

If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type VT_FILETIME or VT_DATE, this helper function extracts the value as a FILETIME using the timezone specified by <i>pstfOut</i>. If the source <b>PROPVARIANT</b> is VT_EMPTY or any other type, this function returns a failure result.

The source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> must be in Coordinated Universal Time (UTC). The PSTF_UTC and PSTF_LOCAL flags allow the calling application to specify what time zone the output should be converted to.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttofiletime">PropVariantToFileTime</a> to access a FILETIME value in a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>.


```cpp
// IPropertyStore *ppropstore;
// Assume variable ppropstore is initialized and valid
PROPVARIANT propvar = {0};
HRESULT hr = ppropstore->GetValue(PKEY_DateModified, &propvar);
if (SUCCEEDED(hr))
{
     // PKEY_DateModified is expected to produce a VT_FILETIME or VT_EMPTY value.
     // PropVariantToFileTime will return a failure code for VT_EMPTY
     FILETIME ftModified;
     hr = PropVariantToFileTime(propvar, PSTF_UTC, &ftModified);
     if (SUCCEEDED(hr))
     {
        // ftModified is now valid and contains a file time in UTC
     }
     else
     {
        // Unable to convert propvar to a FILETIME
     }
     PropVariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromfiletime">InitPropVariantFromFileTime</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttofiletimevector">PropVariantToFileTimeVector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttofiletime">VariantToFileTime</a>