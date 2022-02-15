---
UID: NF:locationapi.ILocation.GetReportInterval
title: ILocation::GetReportInterval (locationapi.h)
description: Retrieves the requested amount of time, in milliseconds, between report events.
helpviewer_keywords: ["GetReportInterval","GetReportInterval method [WinLocation]","GetReportInterval method [WinLocation]","ILocation interface","ILocation interface [WinLocation]","GetReportInterval method","ILocation.GetReportInterval","ILocation::GetReportInterval","WinLocation_COM_Ref.ilocation_getreportinterval","locationapi/ILocation::GetReportInterval"]
old-location: winlocation_com_ref\ilocation_getreportinterval.htm
tech.root: winlocation
ms.assetid: c7bcd665-317c-428a-aa20-0d09c8d7a813
ms.date: 12/05/2018
ms.keywords: GetReportInterval, GetReportInterval method [WinLocation], GetReportInterval method [WinLocation],ILocation interface, ILocation interface [WinLocation],GetReportInterval method, ILocation.GetReportInterval, ILocation::GetReportInterval, WinLocation_COM_Ref.ilocation_getreportinterval, locationapi/ILocation::GetReportInterval
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
 - ILocation::GetReportInterval
 - locationapi/ILocation::GetReportInterval
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
 - ILocation.GetReportInterval
---

# ILocation::GetReportInterval


## -description

<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="/uwp/api/windows.devices.geolocation">Windows.Devices.Geolocation</a> API.
]

Retrieves the requested amount of time, in milliseconds, between report events.

## -parameters

### -param reportType [in]

<b>REFIID</b> that specifies the report type for which to get the interval.

### -param pMilliseconds [out]

The address of a <b>DWORD</b> that receives the report interval value, in milliseconds. If the report is not registered, this will be set to <b>NULL</b>. If this value is set to zero, no minimum interval is specified and your application receives events at the location sensor's default interval.

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
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_STATE)</b></dt>
</dl>
</td>
<td width="60%">
The caller is not registered to receive events for the specified report type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pMilliseconds</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

You must call <a href="/windows/desktop/api/locationapi/nf-locationapi-ilocation-registerforreport">RegisterForReport</a> before calling this method.


#### Examples

The following example demonstrates how to call <b>GetReportInterval</b>.


```

DWORD reportInterval = 0;
HRESULT hr = spLocation->GetReportInterval(IID_ILatLongReport, &reportInterval);
```

## -see-also

<a href="/windows/desktop/api/locationapi/nn-locationapi-ilocation">ILocation</a>