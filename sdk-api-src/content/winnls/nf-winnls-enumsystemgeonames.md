---
UID: NF:winnls.EnumSystemGeoNames
title: EnumSystemGeoNames function (winnls.h)
description: Enumerates the two-letter International Organization for Standardization (ISO) 3166-1 codes or numeric United Nations (UN) Series M, Number 49 (M.49) codes for geographical locations that are available on the operating system.
helpviewer_keywords: ["EnumSystemGeoNames","EnumSystemGeoNames function [Internationalization for Windows Applications]","intl.enumsystemgeonames","winnls/EnumSystemGeoNames"]
old-location: intl\enumsystemgeonames.htm
tech.root: Intl
ms.assetid: 0CB7AE4E-F48A-49A6-A5E8-F151D38CE11E
ms.date: 12/05/2018
ms.keywords: EnumSystemGeoNames, EnumSystemGeoNames function [Internationalization for Windows Applications], intl.enumsystemgeonames, winnls/EnumSystemGeoNames
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EnumSystemGeoNames
 - winnls/EnumSystemGeoNames
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-localization-l1-2-4.dll
 - api-ms-win-core-localization-l1-2-3.dll
 - Kernel32.dll
api_name:
 - EnumSystemGeoNames
---

# EnumSystemGeoNames function


## -description

Enumerates the two-letter International Organization for Standardization (ISO) 3166-1 codes or numeric United Nations (UN) Series M, Number 49  (M.49) codes for geographical locations that are available on the operating system.

## -parameters

### -param geoClass [in]

The geographical location class for which to enumerate the available two-letter ISO 3166-1 or numeric UN M.49 codes.

### -param geoEnumProc [in]

Pointer to the application-defined callback function <a href="/windows/desktop/api/winnls/nc-winnls-geo_enumnameproc">Geo_EnumNameProc</a>. The <b>EnumSystemGeoNames</b> function calls this callback function for each of the two-letter ISO 3166-1 or numeric UN M.49 codes for geographical locations that are available on the operating system until callback function returns <b>FALSE</b>.

### -param data [in, optional]

Application-specific information to pass to the callback function that the <i>genEnumProc</i> parameter specifies.

## -returns

Returns a nonzero value if successful, or 0 otherwise. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The values supplied for flags were not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter value was not valid. 

</td>
</tr>
</table>

## -remarks

For information about two-letter ISO 3166-1 codes, see <a href="https://www.iso.org/iso-3166-country-codes.html">Country Codes - ISO 3166</a>.  For information about numeric UN M.49 codes, see <a href="https://unstats.un.org/unsd/methodology/m49/">Standard country or area codes for statistical use (M49)</a>.

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-enumsystemgeoid">EnumSystemGeoID</a>



<a href="/windows/desktop/api/winnls/nc-winnls-geo_enumnameproc">Geo_EnumNameProc</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>