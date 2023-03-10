---
UID: NF:locationapi.ICivicAddressReport.GetAddressLine2
title: ICivicAddressReport::GetAddressLine2 (locationapi.h)
description: Retrieves the second line of a street address.
helpviewer_keywords: ["GetAddressLine2","GetAddressLine2 method [WinLocation]","GetAddressLine2 method [WinLocation]","ICivicAddressReport interface","ICivicAddressReport interface [WinLocation]","GetAddressLine2 method","ICivicAddressReport.GetAddressLine2","ICivicAddressReport::GetAddressLine2","WinLocation_COM_Ref.icivicaddressreport_getaddressline2","locationapi/ICivicAddressReport::GetAddressLine2"]
old-location: winlocation_com_ref\icivicaddressreport_getaddressline2.htm
tech.root: winlocation
ms.assetid: 2c66b294-15a9-490a-b77c-ff48f35d1d3b
ms.date: 12/05/2018
ms.keywords: GetAddressLine2, GetAddressLine2 method [WinLocation], GetAddressLine2 method [WinLocation],ICivicAddressReport interface, ICivicAddressReport interface [WinLocation],GetAddressLine2 method, ICivicAddressReport.GetAddressLine2, ICivicAddressReport::GetAddressLine2, WinLocation_COM_Ref.icivicaddressreport_getaddressline2, locationapi/ICivicAddressReport::GetAddressLine2
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
 - ICivicAddressReport::GetAddressLine2
 - locationapi/ICivicAddressReport::GetAddressLine2
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
 - ICivicAddressReport.GetAddressLine2
---

# ICivicAddressReport::GetAddressLine2


## -description

<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="/uwp/api/windows.devices.geolocation">Windows.Devices.Geolocation</a> API.
]

Retrieves the second line of a street address.

## -parameters

### -param pbstrAddress2 [out]

Address of a <b>BSTR</b> that receives the second line of a street address.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/locationapi/nn-locationapi-icivicaddressreport">ICivicAddressReport</a>