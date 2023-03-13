---
UID: NE:locationapi.LOCATION_REPORT_STATUS
title: LOCATION_REPORT_STATUS (locationapi.h)
description: Defines possible status for new reports of a particular report type.
helpviewer_keywords: ["LOCATION_REPORT_STATUS","LOCATION_REPORT_STATUS enumeration [WinLocation]","REPORT_ACCESS_DENIED","REPORT_ERROR","REPORT_INITIALIZING","REPORT_NOT_SUPPORTED","REPORT_RUNNING","WinLocation_COM_Ref.location_report_status","locationapi/LOCATION_REPORT_STATUS","locationapi/REPORT_ACCESS_DENIED","locationapi/REPORT_ERROR","locationapi/REPORT_INITIALIZING","locationapi/REPORT_NOT_SUPPORTED","locationapi/REPORT_RUNNING"]
old-location: winlocation_com_ref\location_report_status.htm
tech.root: winlocation
ms.assetid: 440e64cb-d09c-47cd-9434-8d4479fa52e2
ms.date: 12/05/2018
ms.keywords: LOCATION_REPORT_STATUS, LOCATION_REPORT_STATUS enumeration [WinLocation], REPORT_ACCESS_DENIED, REPORT_ERROR, REPORT_INITIALIZING, REPORT_NOT_SUPPORTED, REPORT_RUNNING, WinLocation_COM_Ref.location_report_status, locationapi/LOCATION_REPORT_STATUS, locationapi/REPORT_ACCESS_DENIED, locationapi/REPORT_ERROR, locationapi/REPORT_INITIALIZING, locationapi/REPORT_NOT_SUPPORTED, locationapi/REPORT_RUNNING
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: LOCATION_REPORT_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LOCATION_REPORT_STATUS
 - locationapi/LOCATION_REPORT_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - LocationApi.h
api_name:
 - LOCATION_REPORT_STATUS
---

# LOCATION_REPORT_STATUS enumeration


## -description

<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="/uwp/api/windows.devices.geolocation">Windows.Devices.Geolocation</a> API.
]

Defines possible status for new reports of a particular report type.

## -enum-fields

### -field REPORT_NOT_SUPPORTED:0

The requested report type is not supported by the API. No location providers of the requested type are installed.

### -field REPORT_ERROR:1

There was an error when creating the report, or location providers for the requested type are unable to provide any data. Location providers might be currently unavailable, or location providers cannot obtain any data. For example, this state may occur when a GPS sensor is indoors and no satellites are in view.

### -field REPORT_ACCESS_DENIED:2

 No permissions have been granted to access this report type. Call <a href="/windows/desktop/api/locationapi/nf-locationapi-ilocation-requestpermissions">ILocation::RequestPermissions</a>.

### -field REPORT_INITIALIZING:3

The report is being initialized.

### -field REPORT_RUNNING:4

The report is running. New location data for the requested report type is available.

## -remarks

These values represent status for new reports. The most recent reports remain available through <a href="/windows/desktop/api/locationapi/nf-locationapi-ilocation-getreport">ILocation::GetReport</a>, regardless of the reported status. If the status is <b>REPORT_RUNNING</b>, the data in a report is new. Otherwise, <b>ILocation::GetReport</b> provides cached data if cached data is available.


#### Examples

The following code example demonstrates how to retrieve the <b>LOCATION_REPORT_STATUS</b> values from <a href="/windows/desktop/api/locationapi/nf-locationapi-ilocation-getreportstatus">ILocation::GetReportStatus</a>.


```cpp
    // Get the status of this report type
    if (SUCCEEDED(spLocation->GetReportStatus(IID_ILatLongReport, &status))) 
    {
        bool fIsNotRunning = true;
        switch (status) 
        {
        case REPORT_RUNNING:
            // If the status for the current report is running,
            // then do not print any additional message.
            // Otherwise, print a message indicating that reports may contain cached data.
            fIsNotRunning = false;
            break;
        case REPORT_NOT_SUPPORTED:
            wprintf(L"\nThere is no sensor installed for this report type.\n");
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
        }

        if (true == fIsNotRunning)
        {
            wprintf(L"Location reports returned from GetReport contain cached data.\n");
        }
    }

```


The following code is a sample implementation of the callback function <a href="/windows/desktop/api/locationapi/nf-locationapi-ilocationevents-onstatuschanged">ILocationEvents::OnStatusChanged</a>.  This implementation prints out messages when there is a  change in the status of latitude/longitude reports.


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
