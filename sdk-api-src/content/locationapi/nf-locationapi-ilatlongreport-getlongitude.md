---
UID: NF:locationapi.ILatLongReport.GetLongitude
title: ILatLongReport::GetLongitude (locationapi.h)
description: Retrieves the longitude, in degrees.
helpviewer_keywords: ["GetLongitude","GetLongitude method [WinLocation]","GetLongitude method [WinLocation]","ILatLongReport interface","ILatLongReport interface [WinLocation]","GetLongitude method","ILatLongReport.GetLongitude","ILatLongReport::GetLongitude","WinLocation_COM_Ref.ilatlongreport_getlongitude","locationapi/ILatLongReport::GetLongitude"]
old-location: winlocation_com_ref\ilatlongreport_getlongitude.htm
tech.root: winlocation
ms.assetid: 77fa407b-109c-45aa-bbdb-0b8a40d222e5
ms.date: 12/05/2018
ms.keywords: GetLongitude, GetLongitude method [WinLocation], GetLongitude method [WinLocation],ILatLongReport interface, ILatLongReport interface [WinLocation],GetLongitude method, ILatLongReport.GetLongitude, ILatLongReport::GetLongitude, WinLocation_COM_Ref.ilatlongreport_getlongitude, locationapi/ILatLongReport::GetLongitude
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
 - ILatLongReport::GetLongitude
 - locationapi/ILatLongReport::GetLongitude
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
 - ILatLongReport.GetLongitude
---

# ILatLongReport::GetLongitude


## -description

<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="/uwp/api/windows.devices.geolocation">Windows.Devices.Geolocation</a> API.
]

Retrieves the longitude, in degrees. The longitude is between -180 and 180, where East is positive.

## -parameters

### -param pLongitude [out]

Address of a <b>DOUBLE</b> that receives the longitude.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/locationapi/nn-locationapi-ilatlongreport">ILatLongReport</a>