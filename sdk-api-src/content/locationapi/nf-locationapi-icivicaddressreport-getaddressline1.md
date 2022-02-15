---
UID: NF:locationapi.ICivicAddressReport.GetAddressLine1
title: ICivicAddressReport::GetAddressLine1 (locationapi.h)
description: Retrieves the first line of a street address.
helpviewer_keywords: ["GetAddressLine1","GetAddressLine1 method [WinLocation]","GetAddressLine1 method [WinLocation]","ICivicAddressReport interface","ICivicAddressReport interface [WinLocation]","GetAddressLine1 method","ICivicAddressReport.GetAddressLine1","ICivicAddressReport::GetAddressLine1","WinLocation_COM_Ref.icivicaddressreport_getaddressline1","locationapi/ICivicAddressReport::GetAddressLine1"]
old-location: winlocation_com_ref\icivicaddressreport_getaddressline1.htm
tech.root: winlocation
ms.assetid: 946f0e69-7139-45e9-8da4-755225ce1bd1
ms.date: 12/05/2018
ms.keywords: GetAddressLine1, GetAddressLine1 method [WinLocation], GetAddressLine1 method [WinLocation],ICivicAddressReport interface, ICivicAddressReport interface [WinLocation],GetAddressLine1 method, ICivicAddressReport.GetAddressLine1, ICivicAddressReport::GetAddressLine1, WinLocation_COM_Ref.icivicaddressreport_getaddressline1, locationapi/ICivicAddressReport::GetAddressLine1
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
 - ICivicAddressReport::GetAddressLine1
 - locationapi/ICivicAddressReport::GetAddressLine1
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
 - ICivicAddressReport.GetAddressLine1
---

# ICivicAddressReport::GetAddressLine1


## -description

<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="/uwp/api/windows.devices.geolocation">Windows.Devices.Geolocation</a> API.
]

Retrieves the first line of a street address.

## -parameters

### -param pbstrAddress1 [out]

Address of a <b>BSTR</b> that receives the first line of a street address.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/locationapi/nn-locationapi-icivicaddressreport">ICivicAddressReport</a>