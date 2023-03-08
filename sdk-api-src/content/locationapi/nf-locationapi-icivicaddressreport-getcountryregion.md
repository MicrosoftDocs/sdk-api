---
UID: NF:locationapi.ICivicAddressReport.GetCountryRegion
title: ICivicAddressReport::GetCountryRegion (locationapi.h)
description: Retrieves the two-letter country or region code.
helpviewer_keywords: ["GetCountryRegion","GetCountryRegion method [WinLocation]","GetCountryRegion method [WinLocation]","ICivicAddressReport interface","ICivicAddressReport interface [WinLocation]","GetCountryRegion method","ICivicAddressReport.GetCountryRegion","ICivicAddressReport::GetCountryRegion","WinLocation_COM_Ref.icivicaddressreport_getcountryregion","locationapi/ICivicAddressReport::GetCountryRegion","winlocation.icivicaddressreport_getcountry"]
old-location: winlocation_com_ref\icivicaddressreport_getcountryregion.htm
tech.root: winlocation
ms.assetid: 1bcf7939-e047-412f-874d-18bb5e93e5ec
ms.date: 12/05/2018
ms.keywords: GetCountryRegion, GetCountryRegion method [WinLocation], GetCountryRegion method [WinLocation],ICivicAddressReport interface, ICivicAddressReport interface [WinLocation],GetCountryRegion method, ICivicAddressReport.GetCountryRegion, ICivicAddressReport::GetCountryRegion, WinLocation_COM_Ref.icivicaddressreport_getcountryregion, locationapi/ICivicAddressReport::GetCountryRegion, winlocation.icivicaddressreport_getcountry
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICivicAddressReport::GetCountryRegion
 - locationapi/ICivicAddressReport::GetCountryRegion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - LocationAPI.dll
api_name:
 - ICivicAddressReport.GetCountryRegion
---

# ICivicAddressReport::GetCountryRegion


## -description

<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="/uwp/api/windows.devices.geolocation">Windows.Devices.Geolocation</a> API.
]

Retrieves the two-letter country or region code.

## -parameters

### -param pbstrCountryRegion [out]

Address of a <b>BSTR</b> that receives the country or region code.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The two-letter country or region code is in ISO 3166 format.


#### Examples

The following example demonstrates how to call <b>GetCountryRegion</b>.


```cpp
    hr = pCivicAddressReport->GetCountryRegion(&bstrCountryRegion);
    if (SUCCEEDED(hr)) 
    {
        // Country/Region is an ISO-3166-1 two-letter code.
       wprintf(L"\tCountry/Region:\t%s\n\n", bstrCountryRegion);    
    }       

```

## -see-also

<a href="/windows/desktop/api/locationapi/nn-locationapi-icivicaddressreport">ICivicAddressReport</a>