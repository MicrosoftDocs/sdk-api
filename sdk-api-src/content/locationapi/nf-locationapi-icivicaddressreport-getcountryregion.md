---
UID: NF:locationapi.ICivicAddressReport.GetCountryRegion
title: ICivicAddressReport::GetCountryRegion
author: windows-sdk-content
description: Retrieves the two-letter country or region code.
old-location: winlocation_com_ref\icivicaddressreport_getcountryregion.htm
tech.root: locationapi
ms.assetid: 1bcf7939-e047-412f-874d-18bb5e93e5ec
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetCountryRegion, GetCountryRegion method [WinLocation], GetCountryRegion method [WinLocation],ICivicAddressReport interface, ICivicAddressReport interface [WinLocation],GetCountryRegion method, ICivicAddressReport.GetCountryRegion, ICivicAddressReport::GetCountryRegion, WinLocation_COM_Ref.icivicaddressreport_getcountryregion, locationapi/ICivicAddressReport::GetCountryRegion, winlocation.icivicaddressreport_getcountry
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: locationapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only],Windows 7
req.target-min-winversvr: None supported
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
req.dll: LocationAPI.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - LocationAPI.dll
api_name:
 - ICivicAddressReport.GetCountryRegion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICivicAddressReport::GetCountryRegion


## -description


<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/fd40bf4a-c59a-43a4-ab01-c671a8a41731">Windows.Devices.Geolocation</a>API.
]

Retrieves the two-letter country or region code.


## -parameters




### -param pbstrCountryRegion [out]

Address of a <b>BSTR</b> that receives the country or region code.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The two-letter country or region code is in ISO 3166 format.


#### Examples

The following example demonstrates how to call <b>GetCountryRegion</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    hr = pCivicAddressReport-&gt;GetCountryRegion(&amp;bstrCountryRegion);
    if (SUCCEEDED(hr)) 
    {
        // Country/Region is an ISO-3166-1 two-letter code.
       wprintf(L"\tCountry/Region:\t%s\n\n", bstrCountryRegion);    
    }       
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ba8c66cb-be94-4649-ada9-620ed3b35516">ICivicAddressReport</a>
 

 

