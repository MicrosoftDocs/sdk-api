---
UID: NF:winnls.GetUserDefaultGeoName
title: GetUserDefaultGeoName function (winnls.h)
description: Retrieves the two-letter International Organization for Standardization (ISO) 3166-1 code or numeric United Nations (UN) Series M, Number 49 (M.49) code for the default geographical location of the user.
helpviewer_keywords: ["GetUserDefaultGeoName","GetUserDefaultGeoName function [Internationalization for Windows Applications]","intl.getuserdefaultgeoname","winnls/GetUserDefaultGeoName"]
old-location: intl\getuserdefaultgeoname.htm
tech.root: Intl
ms.assetid: 7938A5A1-E18E-4643-A07C-3354B4E94B5D
ms.date: 12/05/2018
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
 - Kernel32.dll
api_name:
 - GetUserDefaultGeoName
---

# GetUserDefaultGeoName function


## -description

Retrieves the two-letter International Organization for Standardization (ISO) 3166-1 code or numeric United Nations (UN) Series M, Number 49  (M.49) code for the default geographical location of the user.

## -parameters

### -param geoName [out]

Pointer to a buffer in which this function should write the null-terminated two-letter ISO 3166-1 or numeric UN M.49 code for the default geographic location of the user.

### -param geoNameCount [in]

The size of the buffer that the <i>geoName</i> parameter specifies. If this value is zero, the function only returns the number of characters that function would copy to the output buffer, but does not write the name of the default geographic location of the user to the buffer.

## -returns

The number of characters
  the function  would copy to the output buffer, if the value of the <i>geoNameCount</i> parameter is zero. Otherwise, the  number of characters that the function copied to the buffer that the <i>geoName</i> parameter specifies.

Zero indicates that the function failed. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BADDB</b></dt>
</dl>
</td>
<td width="60%">
The function could not read information from the registry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer that the  <i>geoName</i> parameter specifies is too small for the string. 

</td>
</tr>
</table>

## -remarks

For information about two-letter ISO 3166-1 codes, see <a href="https://www.iso.org/iso-3166-country-codes.html">Country Codes - ISO 3166</a>.  For information about numeric UN M.49 codes, see <a href="https://unstats.un.org/unsd/methodology/m49/">Standard country or area codes for statistical use (M49)</a>.

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-getusergeoid">GetUserGeoID</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>



<a href="/windows/desktop/api/winnls/nf-winnls-setusergeoname">SetUserGeoName</a>