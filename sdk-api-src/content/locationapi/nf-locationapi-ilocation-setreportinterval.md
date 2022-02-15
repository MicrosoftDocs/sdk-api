---
UID: NF:locationapi.ILocation.SetReportInterval
title: ILocation::SetReportInterval (locationapi.h)
description: Specifies the requested minimum amount of time, in milliseconds, between report events.
helpviewer_keywords: ["ILocation interface [WinLocation]","SetReportInterval method","ILocation.SetReportInterval","ILocation::SetReportInterval","SetReportInterval","SetReportInterval method [WinLocation]","SetReportInterval method [WinLocation]","ILocation interface","WinLocation_COM_Ref.ilocation_setreportinterval","locationapi/ILocation::SetReportInterval"]
old-location: winlocation_com_ref\ilocation_setreportinterval.htm
tech.root: winlocation
ms.assetid: 4b48f64d-47e8-41cc-a7a1-970654896e7e
ms.date: 12/05/2018
ms.keywords: ILocation interface [WinLocation],SetReportInterval method, ILocation.SetReportInterval, ILocation::SetReportInterval, SetReportInterval, SetReportInterval method [WinLocation], SetReportInterval method [WinLocation],ILocation interface, WinLocation_COM_Ref.ilocation_setreportinterval, locationapi/ILocation::SetReportInterval
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
 - ILocation::SetReportInterval
 - locationapi/ILocation::SetReportInterval
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
 - ILocation.SetReportInterval
---

# ILocation::SetReportInterval


## -description

<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="/uwp/api/windows.devices.geolocation">Windows.Devices.Geolocation</a> API.
]

Specifies the requested minimum amount of time, in milliseconds, between report events.

## -parameters

### -param reportType [in]

<b>REFIID</b> that specifies the report type for which to set the interval.

### -param millisecondsRequested [in]

<b>DWORD</b> that contains the report interval value, in milliseconds. If this value is zero, no minimum interval is specified and your application receives events at the location sensor's default interval.

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
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
<i>reportType</i> was other than <b>IID_ILatLongReport</b> or <b>IID_ICivicAddressReport</b>.

</td>
</tr>
</table>

## -remarks

The interval you request by using this method represents the shortest amount of time between events. This means that you request to receive event notifications no more frequently than specified, but the elapsed time may be significantly longer. Use this method to help ensure that event notifications do not use more processor resources than necessary.

It is not guaranteed that your request for a particular report interval will be set by the location provider. Call <a href="/windows/desktop/api/locationapi/nf-locationapi-ilocation-getreportinterval">GetReportInterval </a> to discover the true report interval setting.

A report interval of zero means that no minimum interval is specified, and the application may receive events at the frequency that the location sensor sends events.


#### Examples

The following example demonstrates how to call <b>SetReportInterval</b>.


```cpp

// Set the latitude/longitude report interval to 1000 milliseconds
HRESULT hr = spLocation->SetReportInterval(IID_ILatLongReport, 1000);
```

## -see-also

<a href="/windows/desktop/api/locationapi/nn-locationapi-ilocation">ILocation</a>