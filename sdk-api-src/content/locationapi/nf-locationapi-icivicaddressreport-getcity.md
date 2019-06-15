---
UID: NF:locationapi.ICivicAddressReport.GetCity
title: ICivicAddressReport::GetCity (locationapi.h)
author: windows-sdk-content
description: Retrieves the city name.
old-location: winlocation_com_ref\icivicaddressreport_getcity.htm
tech.root: locationapi
ms.assetid: c87debb3-63ab-4d5b-85ff-0ee0653d6ffe
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCity, GetCity method [WinLocation], GetCity method [WinLocation],ICivicAddressReport interface, ICivicAddressReport interface [WinLocation],GetCity method, ICivicAddressReport.GetCity, ICivicAddressReport::GetCity, WinLocation_COM_Ref.icivicaddressreport_getcity, locationapi/ICivicAddressReport::GetCity
ms.topic: method
f1_keywords: ["locationapi/ICivicAddressReport.GetCity"]
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
 - ICivicAddressReport.GetCity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICivicAddressReport::GetCity


## -description


<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/en-us/uwp/api/windows.devices.geolocation">Windows.Devices.Geolocation</a>API.
]

Retrieves the city name.


## -parameters




### -param pbstrCity [out]

Address of a <b>BSTR</b> that receives the city name.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/locationapi/nn-locationapi-icivicaddressreport">ICivicAddressReport</a>
 

 

