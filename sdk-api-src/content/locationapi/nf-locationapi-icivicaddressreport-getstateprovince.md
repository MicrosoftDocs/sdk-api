---
UID: NF:locationapi.ICivicAddressReport.GetStateProvince
title: ICivicAddressReport::GetStateProvince (locationapi.h)
description: Retrieves the state or province name.
helpviewer_keywords: ["GetStateProvince","GetStateProvince method [WinLocation]","GetStateProvince method [WinLocation]","ICivicAddressReport interface","ICivicAddressReport interface [WinLocation]","GetStateProvince method","ICivicAddressReport.GetStateProvince","ICivicAddressReport::GetStateProvince","WinLocation_COM_Ref.icivicaddressreport_getstateprovince","locationapi/ICivicAddressReport::GetStateProvince"]
old-location: winlocation_com_ref\icivicaddressreport_getstateprovince.htm
tech.root: winlocation
ms.assetid: 7f47670c-5549-46af-8a16-0e9a43cf90aa
ms.date: 12/05/2018
ms.keywords: GetStateProvince, GetStateProvince method [WinLocation], GetStateProvince method [WinLocation],ICivicAddressReport interface, ICivicAddressReport interface [WinLocation],GetStateProvince method, ICivicAddressReport.GetStateProvince, ICivicAddressReport::GetStateProvince, WinLocation_COM_Ref.icivicaddressreport_getstateprovince, locationapi/ICivicAddressReport::GetStateProvince
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
 - ICivicAddressReport::GetStateProvince
 - locationapi/ICivicAddressReport::GetStateProvince
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
 - ICivicAddressReport.GetStateProvince
---

# ICivicAddressReport::GetStateProvince


## -description

<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="/uwp/api/windows.devices.geolocation">Windows.Devices.Geolocation</a> API.
]

Retrieves the state or province name.

## -parameters

### -param pbstrStateProvince [out]

Address of a <b>BSTR</b> that receives the state or province name.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/locationapi/nn-locationapi-icivicaddressreport">ICivicAddressReport</a>