---
UID: NF:locationapi.ICivicAddressReport.GetCity
title: ICivicAddressReport::GetCity
author: windows-sdk-content
description: Retrieves the city name.
old-location: winlocation_com_ref\icivicaddressreport_getcity.htm
old-project: locationapi
ms.assetid: c87debb3-63ab-4d5b-85ff-0ee0653d6ffe
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: GetCity, GetCity method [WinLocation], GetCity method [WinLocation],ICivicAddressReport interface, ICivicAddressReport interface [WinLocation],GetCity method, ICivicAddressReport.GetCity, ICivicAddressReport::GetCity, WinLocation_COM_Ref.icivicaddressreport_getcity, locationapi/ICivicAddressReport::GetCity
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: LOCATION_REPORT_STATUS
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
req.lib: 
req.dll: LocationAPI.dll
req.irql: 
req.product: GDI+ 1.1
---

# ICivicAddressReport::GetCity


## -description


<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/fd40bf4a-c59a-43a4-ab01-c671a8a41731">Windows.Devices.Geolocation</a>
API.
]

Retrieves the city name.


## -parameters




### -param pbstrCity [out]

Address of a <b>BSTR</b> that receives the city name.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ba8c66cb-be94-4649-ada9-620ed3b35516">ICivicAddressReport</a>
 

 

