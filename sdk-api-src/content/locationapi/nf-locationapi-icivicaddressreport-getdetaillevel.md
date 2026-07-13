---
UID: NF:locationapi.ICivicAddressReport.GetDetailLevel
title: ICivicAddressReport::GetDetailLevel (locationapi.h)
description: Reserved. (ICivicAddressReport.GetDetailLevel)
helpviewer_keywords: ["GetDetailLevel","GetDetailLevel method [WinLocation]","GetDetailLevel method [WinLocation]","ICivicAddressReport interface","ICivicAddressReport interface [WinLocation]","GetDetailLevel method","ICivicAddressReport.GetDetailLevel","ICivicAddressReport::GetDetailLevel","WinLocation_COM_Ref.icivicaddressreport_getdetaillevel","locationapi/ICivicAddressReport::GetDetailLevel"]
old-location: winlocation_com_ref\icivicaddressreport_getdetaillevel.htm
tech.root: winlocation
ms.assetid: ec32dee1-e9ce-40a0-bca0-6f5f767b7604
ms.date: 12/05/2018
ms.keywords: GetDetailLevel, GetDetailLevel method [WinLocation], GetDetailLevel method [WinLocation],ICivicAddressReport interface, ICivicAddressReport interface [WinLocation],GetDetailLevel method, ICivicAddressReport.GetDetailLevel, ICivicAddressReport::GetDetailLevel, WinLocation_COM_Ref.icivicaddressreport_getdetaillevel, locationapi/ICivicAddressReport::GetDetailLevel
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
 - ICivicAddressReport::GetDetailLevel
 - locationapi/ICivicAddressReport::GetDetailLevel
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
 - ICivicAddressReport.GetDetailLevel
---

# ICivicAddressReport::GetDetailLevel


## -description

<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="/uwp/api/windows.devices.geolocation">Windows.Devices.Geolocation</a> API.
]

Reserved.

## -parameters

### -param pDetailLevel [out]

Reserved.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To determine whether a civic address report contains valid data for a particular field, simply inspect the field's contents. If the field contains a value,  you can assume that the field contains the most accurate information available.

## -see-also

<a href="/windows/desktop/api/locationapi/nn-locationapi-icivicaddressreport">ICivicAddressReport</a>
