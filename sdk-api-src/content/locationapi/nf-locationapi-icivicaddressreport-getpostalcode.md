---
UID: NF:locationapi.ICivicAddressReport.GetPostalCode
title: ICivicAddressReport::GetPostalCode (locationapi.h)
description: Retrieves the postal code.
helpviewer_keywords: ["GetPostalCode","GetPostalCode method [WinLocation]","GetPostalCode method [WinLocation]","ICivicAddressReport interface","ICivicAddressReport interface [WinLocation]","GetPostalCode method","ICivicAddressReport.GetPostalCode","ICivicAddressReport::GetPostalCode","WinLocation_COM_Ref.icivicaddressreport_getpostalcode","locationapi/ICivicAddressReport::GetPostalCode"]
old-location: winlocation_com_ref\icivicaddressreport_getpostalcode.htm
tech.root: winlocation
ms.assetid: 1580a1b9-1503-43d8-af1c-3b2ba8e9f81a
ms.date: 12/05/2018
ms.keywords: GetPostalCode, GetPostalCode method [WinLocation], GetPostalCode method [WinLocation],ICivicAddressReport interface, ICivicAddressReport interface [WinLocation],GetPostalCode method, ICivicAddressReport.GetPostalCode, ICivicAddressReport::GetPostalCode, WinLocation_COM_Ref.icivicaddressreport_getpostalcode, locationapi/ICivicAddressReport::GetPostalCode
f1_keywords:
- locationapi/ICivicAddressReport.GetPostalCode
dev_langs:
- c++
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
- ICivicAddressReport.GetPostalCode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICivicAddressReport::GetPostalCode


## -description


<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/uwp/api/windows.devices.geolocation">Windows.Devices.Geolocation</a>API.
]

Retrieves the postal code.


## -parameters




### -param pbstrPostalCode [out]

Address of a <b>BSTR</b> that receives the postal code.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/locationapi/nn-locationapi-icivicaddressreport">ICivicAddressReport</a>
 

 

