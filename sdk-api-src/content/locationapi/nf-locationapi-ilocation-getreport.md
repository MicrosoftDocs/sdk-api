---
UID: NF:locationapi.ILocation.GetReport
title: ILocation::GetReport (locationapi.h)
description: Retrieves a location report.
helpviewer_keywords: ["GetReport","GetReport method [WinLocation]","GetReport method [WinLocation]","ILocation interface","ILocation interface [WinLocation]","GetReport method","ILocation.GetReport","ILocation::GetReport","WinLocation_COM_Ref.ilocation_getreport","locationapi/ILocation::GetReport"]
old-location: winlocation_com_ref\ilocation_getreport.htm
tech.root: winlocation
ms.assetid: 69d0fed5-7f02-4d74-bdbd-3a0fd85e76ed
ms.date: 12/05/2018
ms.keywords: GetReport, GetReport method [WinLocation], GetReport method [WinLocation],ILocation interface, ILocation interface [WinLocation],GetReport method, ILocation.GetReport, ILocation::GetReport, WinLocation_COM_Ref.ilocation_getreport, locationapi/ILocation::GetReport
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
 - ILocation::GetReport
 - locationapi/ILocation::GetReport
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
 - ILocation.GetReport
---

# ILocation::GetReport


## -description

<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="/uwp/api/windows.devices.geolocation">Windows.Devices.Geolocation</a> API.
]

Retrieves a location report.

## -parameters

### -param reportType [in]

<b>REFIID</b> that specifies the type of report to retrieve.

### -param ppLocationReport [out]

Address of a pointer to <a href="/windows/desktop/api/locationapi/nn-locationapi-ilocationreport">ILocationReport</a> that receives the specified location report.

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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The location provider has permissions disabled and report data cannot be retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
<i>reportType </i> is other than <b>IID_ILatLongReport</b> or <b>IID_ICivicAddressReport</b>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NO_DATA)</b></dt>
</dl>
</td>
<td width="60%">
No data is available. This may be due to an error or due to the provider being unavailable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>ppLocationReport</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>reportType </i> is <b>IID_ILatLongReport</b>, and the latitude or longitude value is out of bounds.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The underlying sensor is <b>NULL</b> or disconnected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>

## -remarks

<a href="/windows/desktop/api/locationapi/nn-locationapi-ilocationreport">ILocationReport</a> is the base interface for specific location report types.   Call <b>QueryInterface</b> to retrieve a pointer to the correct report type.

When <b>GetReport</b> is called, it may result in a notification being displayed in the taskbar, and a Location Activity event being logged in Event Viewer, if it is the application's first use of location.

<div class="alert"><b>Note</b>  When an application first starts, or when a new location sensor is enabled, <a href="/windows/desktop/api/locationapi/nf-locationapi-ilocation-getreportstatus">GetReportStatus</a> may report a status of <b>REPORT_RUNNING</b>  shortly before the new location report is available. Therefore, an initial call to <b>GetReport</b> can return an error (<b>ERROR_NO_DATA</b>) or a value that is not from the expected location sensor, even if <b>GetReportStatus</b> indicates a status of <b>REPORT_RUNNING</b>. See <a href="/windows/desktop/api/locationapi/nf-locationapi-ilocation-getreportstatus">GetReportStatus</a> for a description of a workaround for this issue.</div>
<div> </div>

#### Examples

The following example calls <b>GetReport</b> for latitude/longitude reports and demonstrates how to call QueryInterface to retrieve a pointer to the specified report type.


```cpp
CComPtr<ILocationReport> spLocationReport; // This is our location report object
CComPtr<ILatLongReport> spLatLongReport; // This is our LatLong report object

// Get the current latitude/longitude location report,
hr = spLocation->GetReport(IID_ILatLongReport, &spLocationReport);
// then get a pointer to the ILatLongReport interface by calling QueryInterface
if (SUCCEEDED(hr))
{
    hr = spLocationReport->QueryInterface(&spLatLongReport);
}

```