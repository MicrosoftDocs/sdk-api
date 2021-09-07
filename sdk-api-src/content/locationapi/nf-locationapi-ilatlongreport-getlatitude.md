---
UID: NF:locationapi.ILatLongReport.GetLatitude
title: ILatLongReport::GetLatitude (locationapi.h)
description: Retrieves the latitude, in degrees.
helpviewer_keywords: ["GetLatitude","GetLatitude method [WinLocation]","GetLatitude method [WinLocation]","ILatLongReport interface","ILatLongReport interface [WinLocation]","GetLatitude method","ILatLongReport.GetLatitude","ILatLongReport::GetLatitude","WinLocation_COM_Ref.ilatlongreport_getlatitude","locationapi/ILatLongReport::GetLatitude"]
old-location: winlocation_com_ref\ilatlongreport_getlatitude.htm
tech.root: winlocation
ms.assetid: 81392683-61bc-4b17-8f3c-172b66bd543b
ms.date: 12/05/2018
ms.keywords: GetLatitude, GetLatitude method [WinLocation], GetLatitude method [WinLocation],ILatLongReport interface, ILatLongReport interface [WinLocation],GetLatitude method, ILatLongReport.GetLatitude, ILatLongReport::GetLatitude, WinLocation_COM_Ref.ilatlongreport_getlatitude, locationapi/ILatLongReport::GetLatitude
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
 - ILatLongReport::GetLatitude
 - locationapi/ILatLongReport::GetLatitude
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
 - ILatLongReport.GetLatitude
---

# ILatLongReport::GetLatitude


## -description

<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="/uwp/api/windows.devices.geolocation">Windows.Devices.Geolocation</a> API.
]

Retrieves the latitude, in degrees. The latitude is between -90 and 90, where north is positive.

## -parameters

### -param pLatitude [out]

Address of a <b>DOUBLE</b> that receives the latitude.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/locationapi/nn-locationapi-ilatlongreport">ILatLongReport</a>