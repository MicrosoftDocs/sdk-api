---
UID: NF:locationapi.IDefaultLocation.GetReport
title: IDefaultLocation::GetReport (locationapi.h)
description: Retrieves the specified report type from the default location provider.
helpviewer_keywords: ["GetReport","GetReport method [WinLocation]","GetReport method [WinLocation]","IDefaultLocation interface","IDefaultLocation interface [WinLocation]","GetReport method","IDefaultLocation.GetReport","IDefaultLocation::GetReport","WinLocation_COM_Ref.idefaultlocation_getreport","locationapi/IDefaultLocation::GetReport"]
old-location: winlocation_com_ref\idefaultlocation_getreport.htm
tech.root: winlocation
ms.assetid: 7b52dd6e-cba5-4248-b1be-b34e47a029d5
ms.date: 12/05/2018
ms.keywords: GetReport, GetReport method [WinLocation], GetReport method [WinLocation],IDefaultLocation interface, IDefaultLocation interface [WinLocation],GetReport method, IDefaultLocation.GetReport, IDefaultLocation::GetReport, WinLocation_COM_Ref.idefaultlocation_getreport, locationapi/IDefaultLocation::GetReport
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
 - IDefaultLocation::GetReport
 - locationapi/IDefaultLocation::GetReport
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
 - IDefaultLocation.GetReport
---

# IDefaultLocation::GetReport


## -description

<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="/uwp/api/windows.devices.geolocation">Windows.Devices.Geolocation</a> API.
]

Retrieves the specified report type from the default location provider.

## -parameters

### -param reportType [in]

<b>REFIID</b> representing the interface ID for the type of report being retrieved.

### -param ppLocationReport [out]

The address of a pointer to <a href="/windows/desktop/api/locationapi/nn-locationapi-ilocationreport">ILocationReport</a> that receives the specified location report from the default location provider.

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
The location report was successfully retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
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
No data is available. This may be due to a lack of default location data in the registry, corrupt data in the registry, or a missing Country/Region field in the default location report.


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
</table>

## -remarks

<a href="/windows/desktop/api/locationapi/nn-locationapi-ilocationreport">ILocationReport</a> is the base interface for specific location report types. The actual interface you use for <i>ppLocationReport</i> must match the type you specified through <i>reportType</i>.

A call to <b>IDefaultLocation::GetReport</b> may result in a notification being displayed in the taskbar, and a Location Activity event being logged in Event Viewer, if it is the application's first use of location.

## -see-also

<a href="/previous-versions/visualstudio">About Location Notifications</a>



<a href="/previous-versions/visualstudio">About Logging Location Activity</a>



<a href="/windows/desktop/api/locationapi/nn-locationapi-idefaultlocation">IDefaultLocation</a>