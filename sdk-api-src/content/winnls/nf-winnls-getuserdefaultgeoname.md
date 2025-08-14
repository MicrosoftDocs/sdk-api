---
UID: NF:winnls.GetUserDefaultGeoName
title: GetUserDefaultGeoName function (winnls.h)
description: Retrieves the two-letter International Organization for Standardization (ISO) 3166-1 code or numeric United Nations (UN) Series M, Number 49 (M.49) code for the default geographical location of the user.
helpviewer_keywords: ["GetUserDefaultGeoName","GetUserDefaultGeoName function [Internationalization for Windows Applications]","intl.getuserdefaultgeoname","winnls/GetUserDefaultGeoName"]
old-location: intl\getuserdefaultgeoname.htm
tech.root: Intl
ms.assetid: 7938A5A1-E18E-4643-A07C-3354B4E94B5D
ms.date: 01/29/2025
ms.keywords: GetUserDefaultGeoName, GetUserDefaultGeoName function [Internationalization for Windows Applications], intl.getuserdefaultgeoname, winnls/GetUserDefaultGeoName
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
 - GetUserDefaultGeoName
 - winnls/GetUserDefaultGeoName
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
 - GetUserDefaultGeoName
---

# GetUserDefaultGeoName function

## -description

Retrieves the default geographical location of the user as an International Organization for Standardization (ISO) 3166-1 two-letter code, if available. Otherwise, a United Nations (UN) Series M, Number 49 (M.49) numeric code.

## -parameters

### -param geoName [out]

Pointer to a buffer in which this function should write the null-terminated International Organization for Standardization (ISO) 3166-1 two-letter code or a United Nations (UN) Series M, Number 49 (M.49) numeric code.

### -param geoNameCount [in]

The size of the buffer that the *geoName* parameter specifies. If this value is zero, the function only returns the number of characters that function would copy to the output buffer, but does not write the name of the default geographic location of the user to the buffer.

## -returns

The number of characters the function would copy to the output buffer if the value of the *geoNameCount* parameter is zero. Otherwise, the  number of characters that the function copied to the buffer that the *geoName* parameter specifies.

Zero indicates that the function failed. To get extended error information, call [GetLastError](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:

| Return code                | Description                                           |
|----------------------------|-------------------------------------------------------|
| **ERROR_INVALID_PARAMETER**| A parameter value was not valid.                      |
| **ERROR_BADDB**            | The function could not read information from the registry. |
| **ERROR_INSUFFICIENT_BUFFER** | The buffer that the *geoName* parameter specifies is too small for the string. |

## -remarks

If the ISO 3166-1 code for the user's default geographical location is 'XX' (which indicates that no code has been assigned), but the location does have a UN M.49 code assigned, then the M.49 code is returned as a decimal string.

For information about two-letter ISO 3166-1 codes, see [ISO 3166 Country Codes](https://www.iso.org/iso-3166-country-codes.html).

For information about numeric UN M.49 codes, see [Standard country or area codes for statistical use (M49)](https://unstats.un.org/unsd/methodology/m49/).

## -see-also

- [GetUserGeoID](/windows/desktop/api/winnls/nf-winnls-getusergeoid)
- [National Language Support](/windows/desktop/Intl/national-language-support)
- [National Language Support Functions](/windows/desktop/Intl/national-language-support-functions)
- [SetUserGeoName](/windows/desktop/api/winnls/nf-winnls-setusergeoname)
