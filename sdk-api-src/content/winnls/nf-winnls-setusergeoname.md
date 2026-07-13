---
UID: NF:winnls.SetUserGeoName
title: SetUserGeoName function (winnls.h)
description: Sets the geographic location for the current user to the specified two-letter International Organization for Standardization (ISO) 3166-1 code or numeric United Nations (UN) Series M, Number 49 (M.49) code.
helpviewer_keywords: ["SetUserGeoName","SetUserGeoName function [Internationalization for Windows Applications]","intl.setusergeoname","winnls/SetUserGeoName"]
old-location: intl\setusergeoname.htm
tech.root: Intl
ms.assetid: 0E5934DE-F526-45B4-9DAF-C8941F00C162
ms.date: 12/05/2018
ms.keywords: SetUserGeoName, SetUserGeoName function [Internationalization for Windows Applications], intl.setusergeoname, winnls/SetUserGeoName
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
 - SetUserGeoName
 - winnls/SetUserGeoName
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
 - SetUserGeoName
---

# SetUserGeoName function


## -description

Sets the geographic location for the current user to the specified two-letter International Organization for Standardization (ISO) 3166-1 code or numeric United Nations (UN) Series M, Number 49  (M.49) code.

## -parameters

### -param geoName [in]

The two-letter ISO 3166-1 or numeric UN M.49 code for the geographic location to set for the current user. To get the codes that are available on the operating system, call <a href="/windows/desktop/api/winnls/nf-winnls-enumsystemgeonames">EnumSystemGeoNames</a>.

## -returns

Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise.

If this function does not succeed, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DISABLED_BY_POLICY</b></dt>
</dl>
</td>
<td width="60%">
The group policy of the computer or the user has forbidden this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INTERNAL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error occurred in the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter value was invalid.

</td>
</tr>
</table>

## -remarks

This function writes to the registry the geographical location for a particular user instead of a particular application. This action affects the behavior of other applications that the user runs. As a rule, call this function only when the user has explicitly requested changes, but not for purely application-specific reasons.

For information about two-letter ISO 3166-1 codes, see <a href="https://www.iso.org/iso-3166-country-codes.html">Country Codes - ISO 3166</a>.  For information about numeric UN M.49 codes, see <a href="https://unstats.un.org/unsd/methodology/m49/">Standard country or area codes for statistical use (M49)</a>.

<b>SetUserGeoName</b> is intended for use by applications that are designed to change user settings, such as in Windows Settings. Other applications should not call this function.

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-enumsystemgeonames">EnumSystemGeoNames</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getuserdefaultgeoname">GetUserDefaultGeoName</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>



<a href="/windows/desktop/api/winnls/nf-winnls-setusergeoid">SetUserGeoID</a>