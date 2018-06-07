---
UID: NF:ras.RasGetCountryInfoW
title: RasGetCountryInfoW function
author: windows-sdk-content
description: The RasGetCountryInfo function retrieves country/region-specific dialing information from the Windows Telephony list of countries/regions.
old-location: rras\rasgetcountryinfo.htm
old-project: RRAS
ms.assetid: 87a4ae40-6750-46cf-89c2-c229de5a585d
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: RasGetCountryInfo, RasGetCountryInfo function [RAS], RasGetCountryInfoA, RasGetCountryInfoW, _ras_rasgetcountryinfo, ras/RasGetCountryInfo, ras/RasGetCountryInfoA, ras/RasGetCountryInfoW, rras.rasgetcountryinfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: RASPROJECTION_INFO_TYPE
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
product: Windows
targetos: Windows
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# RasGetCountryInfoW function


## -description


The 
<b>RasGetCountryInfo</b> function retrieves country/region-specific dialing information from the Windows Telephony list of countries/regions.

For more information about country/region-specific dialing information and <a href="https://www.bing.com/search?q=Telephony+Application+Programming+Interface+(TAPI)">Telephony Application Programming Interface (TAPI)</a> country/region identifiers, see the TAPI portion of the Platform Software Development Kit (SDK).


## -parameters




### -param

TBD




#### - lpRasCtryInfo [in, out]

Pointer to a 
<a href="https://msdn.microsoft.com/bab86167-b56c-4467-8950-d892161dfccb">RASCTRYINFO</a> structure that, on output, receives the country/region-specific dialing information followed by additional bytes for a country/region description string. 




On input, set the <b>dwSize</b> member of the structure to sizeof(<a href="https://msdn.microsoft.com/bab86167-b56c-4467-8950-d892161dfccb">RASCTRYINFO</a>) to identify the version of the structure. Also, set the <b>dwCountryId</b> member to the TAPI country/region identifier of the country/region for which to get information.

Allocate at least 256 bytes for the buffer.


#### - lpdwSize [in, out]

Pointer to a variable that, on input, specifies the size, in bytes, of the buffer pointed to by the <i>lpRasCtryInfo</i> parameter. 




On output, this variable receives the number of bytes required.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from <a href="https://msdn.microsoft.com/1fa41438-7c93-4e9c-851c-652fba23da4f">Routing and Remote Access Error Codes</a> or Winerror.h.

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
<a href="https://msdn.microsoft.com/bab86167-b56c-4467-8950-d892161dfccb">RASCTRYINFO</a> structure to 1 in the initial 
<b>RasGetCountryInfo</b> call. This causes the function to return information for the first country/region in the list. The value returned in the <b>dwNextCountryID</b> member is the country/region identifier of the next country/region in the list. Use this value in repeated calls to 
<b>RasGetCountryInfo</b> until <b>dwNextCountryID</b> returns zero, indicating the last country/region in the list.




## -see-also




<a href="https://msdn.microsoft.com/bab86167-b56c-4467-8950-d892161dfccb">RASCTRYINFO</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

