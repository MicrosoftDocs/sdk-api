---
UID: NF:ras.RasGetCountryInfoW
title: RasGetCountryInfoW function (ras.h)
description: The RasGetCountryInfo function retrieves country/region-specific dialing information from the Windows Telephony list of countries/regions. (Unicode)
helpviewer_keywords: ["RasGetCountryInfo", "RasGetCountryInfo function [RAS]", "RasGetCountryInfoW", "_ras_rasgetcountryinfo", "ras/RasGetCountryInfo", "ras/RasGetCountryInfoW", "rras.rasgetcountryinfo"]
old-location: rras\rasgetcountryinfo.htm
tech.root: RRAS
ms.assetid: 87a4ae40-6750-46cf-89c2-c229de5a585d
ms.date: 12/05/2018
ms.keywords: RasGetCountryInfo, RasGetCountryInfo function [RAS], RasGetCountryInfoA, RasGetCountryInfoW, _ras_rasgetcountryinfo, ras/RasGetCountryInfo, ras/RasGetCountryInfoA, ras/RasGetCountryInfoW, rras.rasgetcountryinfo
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasGetCountryInfoW (Unicode) and RasGetCountryInfoA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RasGetCountryInfoW
 - ras/RasGetCountryInfoW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rasapi32.dll
api_name:
 - RasGetCountryInfo
 - RasGetCountryInfoA
 - RasGetCountryInfoW
---

# RasGetCountryInfoW function


## -description

The 
<b>RasGetCountryInfo</b> function retrieves country/region-specific dialing information from the Windows Telephony list of countries/regions.

For more information about country/region-specific dialing information and <a href="/windows/desktop/Tapi/telephony-application-programming-interfaces">Telephony Application Programming Interface (TAPI)</a> country/region identifiers, see the TAPI portion of the Platform Software Development Kit (SDK).

## -parameters

### -param unnamedParam1 [in, out]

Pointer to a 
<a href="/previous-versions/windows/desktop/legacy/aa376731(v=vs.85)">RASCTRYINFO</a> structure that, on output, receives the country/region-specific dialing information followed by additional bytes for a country/region description string. 




On input, set the <b>dwSize</b> member of the structure to sizeof(<a href="/previous-versions/windows/desktop/legacy/aa376731(v=vs.85)">RASCTRYINFO</a>) to identify the version of the structure. Also, set the <b>dwCountryId</b> member to the TAPI country/region identifier of the country/region for which to get information.

Allocate at least 256 bytes for the buffer.

### -param unnamedParam2 [in, out]

Pointer to a variable that, on input, specifies the size, in bytes, of the buffer pointed to by the <i>lpRasCtryInfo</i> parameter. 




On output, this variable receives the number of bytes required.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from <a href="/windows/desktop/RRAS/routing-and-remote-access-error-codes">Routing and Remote Access Error Codes</a> or Winerror.h.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_USER_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The address or buffer specified by <i>lpRasCtryInfo</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <b>dwCountryId</b> member of the structure pointed to by <i>lpRasCtryInfo</i> was not a valid value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUFFER_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The size of the <i>lpRasCtryInfo</i> buffer specified by the <i>lpdwSize</i> parameter was not large enough to store the information for the country/region identified by the <b>dwCountryId</b> member. The function returns the required buffer size in the variable pointed to by <i>lpdwSize</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_TAPI_CONFIGURATION</b></dt>
</dl>
</td>
<td width="60%">
TAPI subsystem information was corrupted.

</td>
</tr>
</table>

## -remarks

To enumerate information for all countries/regions in the Windows Telephony list, set the <b>dwCountryId</b> member of the 
<a href="/previous-versions/windows/desktop/legacy/aa376731(v=vs.85)">RASCTRYINFO</a> structure to 1 in the initial 
<b>RasGetCountryInfo</b> call. This causes the function to return information for the first country/region in the list. The value returned in the <b>dwNextCountryID</b> member is the country/region identifier of the next country/region in the list. Use this value in repeated calls to 
<b>RasGetCountryInfo</b> until <b>dwNextCountryID</b> returns zero, indicating the last country/region in the list.





> [!NOTE]
> The ras.h header defines RasGetCountryInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa376731(v=vs.85)">RASCTRYINFO</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>
