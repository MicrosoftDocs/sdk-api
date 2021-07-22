---
UID: NF:propvarutil.VariantToDosDateTime
title: VariantToDosDateTime function (propvarutil.h)
description: Extracts a date and time value in Microsoft MS-DOS format from a VARIANT structure.
helpviewer_keywords: ["VariantToDosDateTime","VariantToDosDateTime function [Windows Properties]","_shell_VariantToDosDateTime","properties.VariantToDosDateTime","propvarutil/VariantToDosDateTime","shell.VariantToDosDateTime"]
old-location: properties\VariantToDosDateTime.htm
tech.root: properties
ms.assetid: ebbba4d9-8e97-422d-b52f-67c417f295cc
ms.date: 12/05/2018
ms.keywords: VariantToDosDateTime, VariantToDosDateTime function [Windows Properties], _shell_VariantToDosDateTime, properties.VariantToDosDateTime, propvarutil/VariantToDosDateTime, shell.VariantToDosDateTime
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
 - VariantToDosDateTime
 - propvarutil/VariantToDosDateTime
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
 - VariantToDosDateTime
---

# VariantToDosDateTime function


## -description

Extracts a date and time value in Microsoft MS-DOS format from a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure.

## -parameters

### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure.

### -param pwDate [out]

Type: <b>WORD*</b>

When this function returns, contains the extracted <b>WORD</b> that represents a MS-DOS date.

### -param pwTime [out]

Type: <b>WORD*</b>

When this function returns, contains the extracted contains the extracted <b>WORD</b> that represents a MS-DOS time.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This helper function is used when the calling application expects a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> to hold a datetime value.

If the source <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> is of type <b>VT_DATE</b>, this function extracts the datetime value.

If the source <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> is not of type <b>VT_DATE</b>, the function attempts to convert the value in the <b>VARIANT</b> structure into the right format. If a conversion is not possible, <a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttodosdatetime">VariantToDosDateTime</a> returns a failure code. See <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a> for a list of possible conversions.

See <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dosdatetimetovarianttime">DosDateTimeToVariantTime</a> for more information about the formats of <i>pwDate</i>, <i>pwTime</i>, and the source datetime value.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttodosdatetime">VariantToDosDateTime</a> to access a datetime value in a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a>.


```cpp
// VARIANT var;
// Assume variable var is initialize and valid.
// The application expects var to hold a VT_DATE value.

WORD wDate;
WORD wTime;

HRESULT hr = VariantToDosDateTime(var, &wDate, &wTime);

if (SUCCEEDED(hr))
{
    // wDate and wTime are now valid.
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromdosdatetime">InitVariantFromDosDateTime</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttofiletime">PropVariantToFileTime</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttofiletime">VariantToFileTime</a>