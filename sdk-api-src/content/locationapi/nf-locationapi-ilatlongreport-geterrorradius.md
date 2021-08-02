---
UID: NF:locationapi.ILatLongReport.GetErrorRadius
title: ILatLongReport::GetErrorRadius (locationapi.h)
description: Retrieves a distance from the reported location, in meters. Combined with the location reported as the origin, this radius describes the circle in which the actual location is probably located.
helpviewer_keywords: ["GetErrorRadius","GetErrorRadius method [WinLocation]","GetErrorRadius method [WinLocation]","ILatLongReport interface","ILatLongReport interface [WinLocation]","GetErrorRadius method","ILatLongReport.GetErrorRadius","ILatLongReport::GetErrorRadius","WinLocation_COM_Ref.ilatlongreport_geterrorradius","locationapi/ILatLongReport::GetErrorRadius"]
old-location: winlocation_com_ref\ilatlongreport_geterrorradius.htm
tech.root: winlocation
ms.assetid: cb0941da-607d-4082-ac8c-91d2edafa8ab
ms.date: 12/05/2018
ms.keywords: GetErrorRadius, GetErrorRadius method [WinLocation], GetErrorRadius method [WinLocation],ILatLongReport interface, ILatLongReport interface [WinLocation],GetErrorRadius method, ILatLongReport.GetErrorRadius, ILatLongReport::GetErrorRadius, WinLocation_COM_Ref.ilatlongreport_geterrorradius, locationapi/ILatLongReport::GetErrorRadius
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
 - ILatLongReport::GetErrorRadius
 - locationapi/ILatLongReport::GetErrorRadius
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
 - ILatLongReport.GetErrorRadius
---

# ILatLongReport::GetErrorRadius


## -description

<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="/uwp/api/windows.devices.geolocation">Windows.Devices.Geolocation</a> API.
]

Retrieves a distance from the reported location, in meters. Combined with the location reported as the origin, this radius describes the circle in which the actual location is probably located.

## -parameters

### -param pErrorRadius [out]

Address of a <b>DOUBLE</b> that receives the error radius.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/locationapi/nn-locationapi-ilatlongreport">ILatLongReport</a>