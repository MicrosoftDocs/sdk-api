---
UID: NF:locationapi.ILocationEvents.OnStatusChanged
title: ILocationEvents::OnStatusChanged (locationapi.h)
description: Called when a report status changes.
helpviewer_keywords: ["ILocationEvents interface [WinLocation]","OnStatusChanged method","ILocationEvents.OnStatusChanged","ILocationEvents::OnStatusChanged","OnStatusChanged","OnStatusChanged method [WinLocation]","OnStatusChanged method [WinLocation]","ILocationEvents interface","WinLocation_COM_Ref.ilocationevents_onstatuschanged","locationapi/ILocationEvents::OnStatusChanged"]
old-location: winlocation_com_ref\ilocationevents_onstatuschanged.htm
tech.root: winlocation
ms.assetid: d13d8b72-3188-479f-a70c-52b1a9435b80
ms.date: 12/05/2018
ms.keywords: ILocationEvents interface [WinLocation],OnStatusChanged method, ILocationEvents.OnStatusChanged, ILocationEvents::OnStatusChanged, OnStatusChanged, OnStatusChanged method [WinLocation], OnStatusChanged method [WinLocation],ILocationEvents interface, WinLocation_COM_Ref.ilocationevents_onstatuschanged, locationapi/ILocationEvents::OnStatusChanged
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
 - ILocationEvents::OnStatusChanged
 - locationapi/ILocationEvents::OnStatusChanged
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
 - ILocationEvents.OnStatusChanged
---

# ILocationEvents::OnStatusChanged


## -description

<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="/uwp/api/windows.devices.geolocation">Windows.Devices.Geolocation</a> API.
]

Called when a report status changes.

## -parameters

### -param reportType [in]

<b>REFIID</b> that specifies the interface ID of the report type for which the status has changed.

### -param newStatus [in]

A constant from the <a href="/windows/desktop/api/locationapi/ne-locationapi-location_report_status">LOCATION_REPORT_STATUS</a> enumeration that contains the new status.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This event provides report status for new reports. The most recent reports remain available through <a href="/windows/desktop/api/locationapi/nf-locationapi-ilocation-getreport">ILocation::GetReport</a>, regardless of the status reported by this event.


#### Examples

The following is a sample implementation of <b>OnStatusChanged</b> that handles status changed events for latitude/longitude reports.


```cpp
// This is called when the status of a report type changes.
// The LOCATION_REPORT_STATUS enumeration is defined in LocApi.h in the SDK
STDMETHODIMP CLocationEvents::OnStatusChanged(REFIID reportType, LOCATION_REPORT_STATUS status)
{
    if (IID_ILatLongReport == reportType)
    {
        switch (status)
        {
        case REPORT_NOT_SUPPORTED:
            wprintf(L"\nNo devices detected.\n");
            break;
        case REPORT_ERROR:
            wprintf(L"\nReport error.\n");
            break;
        case REPORT_ACCESS_DENIED:
            wprintf(L"\nAccess denied to reports.\n");
            break;
        case REPORT_INITIALIZING:
            wprintf(L"\nReport is initializing.\n");
            break;
        case REPORT_RUNNING:
            wprintf(L"\nRunning.\n");
            break;
        }
    }
    else if (IID_ICivicAddressReport == reportType)
    {
    }

    return S_OK;
}

```

## -see-also

<a href="/windows/desktop/api/locationapi/nn-locationapi-ilocationevents">ILocationEvents</a>