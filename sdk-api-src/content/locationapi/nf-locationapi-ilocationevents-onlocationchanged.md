---
UID: NF:locationapi.ILocationEvents.OnLocationChanged
title: ILocationEvents::OnLocationChanged (locationapi.h)
description: Called when a new location report is available.
helpviewer_keywords: ["ILocationEvents interface [WinLocation]","OnLocationChanged method","ILocationEvents.OnLocationChanged","ILocationEvents::OnLocationChanged","OnLocationChanged","OnLocationChanged method [WinLocation]","OnLocationChanged method [WinLocation]","ILocationEvents interface","WinLocation_COM_Ref.ilocationevents_onlocationchanged","locationapi/ILocationEvents::OnLocationChanged"]
old-location: winlocation_com_ref\ilocationevents_onlocationchanged.htm
tech.root: winlocation
ms.assetid: 14353c8e-15f5-493b-9b49-139924f2397e
ms.date: 12/05/2018
ms.keywords: ILocationEvents interface [WinLocation],OnLocationChanged method, ILocationEvents.OnLocationChanged, ILocationEvents::OnLocationChanged, OnLocationChanged, OnLocationChanged method [WinLocation], OnLocationChanged method [WinLocation],ILocationEvents interface, WinLocation_COM_Ref.ilocationevents_onlocationchanged, locationapi/ILocationEvents::OnLocationChanged
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
 - ILocationEvents::OnLocationChanged
 - locationapi/ILocationEvents::OnLocationChanged
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
 - ILocationEvents.OnLocationChanged
---

# ILocationEvents::OnLocationChanged


## -description

<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="/uwp/api/windows.devices.geolocation">Windows.Devices.Geolocation</a> API.
]

Called when a new location report is available.

## -parameters

### -param reportType [in]

<b>REFIID</b> that contains the interface ID of the report type contained in <i>pLocationReport</i>.

### -param pLocationReport [in]

Pointer to the <a href="/windows/desktop/api/locationapi/nn-locationapi-ilocationreport">ILocationReport</a> instance that contains the new location report.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<a href="/windows/desktop/api/locationapi/nn-locationapi-ilocationreport">ILocationReport</a> is the base interface of specific location report types. The actual interface that the caller receives for <i>pLocationReport</i> will match the type specified by <i>reportType</i>.

If the application calls <b>OnLocationChanged</b> as a result of its first use of location, the call might cause a notification to appear in the taskbar, and cause a Location Activity event to be logged in Event Viewer.   

<div class="alert"><b>Note</b>  An application does not receive the expected location change event from <b>OnLocationChanged</b> if both of the following conditions are true. First, the application runs as a service, in the context of the LOCALSERVICE, SYSTEM, or NETWORKSERVICE user account. Second, the location change event results from changing the default location, either manually when the user selects <b>Default Location</b> in Control Panel, or programmatically when an application calls <a href="/windows/desktop/api/locationapi/nn-locationapi-idefaultlocation">IDefaultLocation::SetReport</a>.</div>
<div> </div>

#### Examples

The following sample implementation of <b>OnLocationChanged</b> handles the location change event for a latitude/longitude report. This implementation prints the following information about a latitude/longitude location change event: the timestamp, the sensor ID, the latitude,  the longitude, the error radius, the altitude, and the altitude error.


```cpp
// This is called when there is a new location report
STDMETHODIMP CLocationEvents::OnLocationChanged(REFIID reportType, ILocationReport* pLocationReport)
{
    // If the report type is a Latitude/Longitude report (as opposed to IID_ICivicAddressReport or another type)
    if (IID_ILatLongReport == reportType)
    {
        CComPtr<ILatLongReport> spLatLongReport;

        // Get the ILatLongReport interface from ILocationReport
        if ((SUCCEEDED(pLocationReport->QueryInterface(IID_PPV_ARGS(&spLatLongReport)))) && (NULL != spLatLongReport.p))
        {
            // Print the Report Type GUID
            wchar_t szGUID[64];
            wprintf(L"\nReportType: %s", GUIDToString(IID_ILatLongReport, szGUID, ARRAYSIZE(szGUID)));

            // Print the Timestamp and the time since the last report
            SYSTEMTIME systemTime;
            if (SUCCEEDED(spLatLongReport->GetTimestamp(&systemTime)))
            {
                // Compute the number of 100ns units that difference between the current report's time and the previous report's time.
                ULONGLONG currentTime = 0, diffTime = 0;
                if (TRUE == SystemTimeToFileTime(&systemTime, (FILETIME*)&currentTime))
                {
                    diffTime = (currentTime > m_previousTime) ? (currentTime - m_previousTime) : 0;
                }

                wprintf(L"\nTimestamp: YY:%d, MM:%d, DD:%d, HH:%d, MM:%d, SS:%d, MS:%d [%I64d]\n",
                    systemTime.wYear,
                    systemTime.wMonth,
                    systemTime.wDay,
                    systemTime.wHour,
                    systemTime.wMinute,
                    systemTime.wSecond,
                    systemTime.wMilliseconds,
                    diffTime / 10000); // Display in milliseconds

                m_previousTime = currentTime; // Set the previous time to the current time for the next report.
            }

            // Print the Sensor ID GUID
            GUID sensorID = {0};
            if (SUCCEEDED(spLatLongReport->GetSensorID(&sensorID)))
            {
                wchar_t szGUID[64];
                wprintf(L"SensorID: %s\n", GUIDToString(sensorID, szGUID, ARRAYSIZE(szGUID)));
            }

            DOUBLE latitude = 0, longitude = 0, altitude = 0, errorRadius = 0, altitudeError = 0;

            // Print the Latitude
            if (SUCCEEDED(spLatLongReport->GetLatitude(&latitude)))
            {
                wprintf(L"Latitude: %f\n", latitude);
            }

            // Print the Longitude
            if (SUCCEEDED(spLatLongReport->GetLongitude(&longitude)))
            {
                wprintf(L"Longitude: %f\n", longitude);
            }

            // Print the Altitude
            if (SUCCEEDED(spLatLongReport->GetAltitude(&altitude)))
            {
                wprintf(L"Altitude: %f\n", altitude);
            }
            else
            {
                // Altitude is optional and may not be available
                wprintf(L"Altitude: Not available.\n");
            }

            // Print the Error Radius
            if (SUCCEEDED(spLatLongReport->GetErrorRadius(&errorRadius)))
            {
                wprintf(L"Error Radius: %f\n", errorRadius);
            }

            // Print the Altitude Error
            if (SUCCEEDED(spLatLongReport->GetAltitudeError(&altitudeError)))
            {
                wprintf(L"Altitude Error: %f\n", altitudeError);
            }
            else
            {
                // Altitude Error is optional and may not be available
                wprintf(L"Altitude Error: Not available.\n");
            }
        }
    }

    return S_OK;
}

```