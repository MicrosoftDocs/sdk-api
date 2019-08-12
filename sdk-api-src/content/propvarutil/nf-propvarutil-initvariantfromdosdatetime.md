---
UID: NF:propvarutil.InitVariantFromDosDateTime
title: InitVariantFromDosDateTime function (propvarutil.h)
author: windows-sdk-content
description: Initializes a VARIANT structure with a date and time given in the format used by Microsoft MS-DOS. The date and time values are converted to the format used to store date and time in a VARIANT.
old-location: properties\InitVariantFromDosDateTime.htm
tech.root: properties
ms.assetid: deb1b3e6-4e7b-49c2-a4dc-e3dfaa2727a0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: InitVariantFromDosDateTime, InitVariantFromDosDateTime function [Windows Properties], _shell_InitVariantFromDosDateTime, properties.InitVariantFromDosDateTime, propvarutil/InitVariantFromDosDateTime, shell.InitVariantFromDosDateTime
ms.topic: function
f1_keywords: 
 - "propvarutil/InitVariantFromDosDateTime"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Propvarutil.h
api_name:
 - InitVariantFromDosDateTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# InitVariantFromDosDateTime function


## -description


Initializes a <a href="https://docs.microsoft.com/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure with a date and time given in the format used by Microsoft MS-DOS. The date and time values are converted to the format used to store date and time in a <b>VARIANT</b>.


## -parameters




### -param wDate [in]

Type: <b>WORD</b>

<b>WORD</b> value that represents an MS-DOS date. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dosdatetimetovarianttime">DosDateTimeToVariantTime</a> for more information about this format.


### -param wTime [in]

Type: <b>WORD</b>

<b>WORD</b> value that represents an MS-DOS time. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dosdatetimetovarianttime">DosDateTimeToVariantTime</a> for more information about this format.


### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="https://docs.microsoft.com/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a <b>VT_DATE</b> variant.

See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dosdatetimetovarianttime">DosDateTimeToVariantTime</a> for more information about the formats of <i>wDate</i>, <i>wTime</i>, and of the resulting variant date.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromdosdatetime">InitVariantFromDosDateTime</a>.


```cpp
// WORD wDate, wTime;
// Assume variables wDate and wTime are initialized and valid.
VARIANT var;

HRESULT hr = InitVariantFromDosDateTime(wDate, wTime, &var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_DATE.
    VariantClear(&propvar);
}
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromfiletime">InitPropVariantFromFileTime</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromfiletime">InitVariantFromFileTime</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-varianttodosdatetime">VariantToDosDateTime</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-varianttofiletime">VariantToFileTime</a>
 

 

