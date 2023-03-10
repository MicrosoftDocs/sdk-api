---
UID: NF:locationapi.ILatLongReport.GetAltitudeError
title: ILatLongReport::GetAltitudeError (locationapi.h)
description: Retrieves the altitude error, in meters.
helpviewer_keywords: ["GetAltitudeError","GetAltitudeError method [WinLocation]","GetAltitudeError method [WinLocation]","ILatLongReport interface","ILatLongReport interface [WinLocation]","GetAltitudeError method","ILatLongReport.GetAltitudeError","ILatLongReport::GetAltitudeError","WinLocation_COM_Ref.ilatlongreport_getaltitudeerror","locationapi/ILatLongReport::GetAltitudeError"]
old-location: winlocation_com_ref\ilatlongreport_getaltitudeerror.htm
tech.root: winlocation
ms.assetid: 313aefda-785c-43ce-a71c-cacfd929e27e
ms.date: 12/05/2018
ms.keywords: GetAltitudeError, GetAltitudeError method [WinLocation], GetAltitudeError method [WinLocation],ILatLongReport interface, ILatLongReport interface [WinLocation],GetAltitudeError method, ILatLongReport.GetAltitudeError, ILatLongReport::GetAltitudeError, WinLocation_COM_Ref.ilatlongreport_getaltitudeerror, locationapi/ILatLongReport::GetAltitudeError
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
 - ILatLongReport::GetAltitudeError
 - locationapi/ILatLongReport::GetAltitudeError
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
 - ILatLongReport.GetAltitudeError
---

# ILatLongReport::GetAltitudeError


## -description

<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="/uwp/api/windows.devices.geolocation">Windows.Devices.Geolocation</a>
API.
]

Retrieves the altitude error, in meters.

## -parameters

### -param pAltitudeError [out]

Address of a <b>DOUBLE</b> that receives the altitude error, in meters. May be <b>NULL</b>.

## -returns

Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
The method returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>HRESULT_FROM_WIN32(ERROR_NO_DATA)</dt>
</dl>
</td>
<td width="60%">
The location report does not include data for the requested field. This result is returned when the location sensor does not support altitude.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/locationapi/nn-locationapi-ilatlongreport">ILatLongReport</a>