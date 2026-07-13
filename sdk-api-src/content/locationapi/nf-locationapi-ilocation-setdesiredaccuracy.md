---
UID: NF:locationapi.ILocation.SetDesiredAccuracy
title: ILocation::SetDesiredAccuracy (locationapi.h)
description: Specifies the accuracy to be used.
helpviewer_keywords: ["ILocation interface [WinLocation]","SetDesiredAccuracy method","ILocation.SetDesiredAccuracy","ILocation::SetDesiredAccuracy","SetDesiredAccuracy","SetDesiredAccuracy method [WinLocation]","SetDesiredAccuracy method [WinLocation]","ILocation interface","locationapi/ILocation::SetDesiredAccuracy","winlocation.ilocation_setdesiredaccuracy"]
old-location: winlocation\ilocation_setdesiredaccuracy.htm
tech.root: winlocation
ms.assetid: 85623570-3b48-42ea-babd-fe4282629d92
ms.date: 12/05/2018
ms.keywords: ILocation interface [WinLocation],SetDesiredAccuracy method, ILocation.SetDesiredAccuracy, ILocation::SetDesiredAccuracy, SetDesiredAccuracy, SetDesiredAccuracy method [WinLocation], SetDesiredAccuracy method [WinLocation],ILocation interface, locationapi/ILocation::SetDesiredAccuracy, winlocation.ilocation_setdesiredaccuracy
req.header: locationapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
 - ILocation::SetDesiredAccuracy
 - locationapi/ILocation::SetDesiredAccuracy
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
 - ILocation.SetDesiredAccuracy
---

# ILocation::SetDesiredAccuracy


## -description

<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="/uwp/api/windows.devices.geolocation">Windows.Devices.Geolocation</a> API.
]

Specifies the accuracy to be used.

## -parameters

### -param reportType [in]

<b>REFIID</b> that specifies the report type for which to set the accuracy to be used.

### -param desiredAccuracy [in]

<a href="/previous-versions/windows/desktop/legacy/dd756639(v=vs.85)">LOCATION_DESIRED_ACCURACY</a> value that specifies the accuracy to be used.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
<i>reportType</i> was other than <b>IID_ILatLongReport</b> or <b>IID_ICivicAddressReport</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>desiredAccuracy</i> is not supported in the <a href="/previous-versions/windows/desktop/legacy/dd756639(v=vs.85)">LOCATION_DESIRED_ACCURACY</a> enumerated type.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/locationapi/nn-locationapi-ilocation">ILocation</a>