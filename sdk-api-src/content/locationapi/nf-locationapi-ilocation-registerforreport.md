---
UID: NF:locationapi.ILocation.RegisterForReport
title: ILocation::RegisterForReport (locationapi.h)
description: Requests location report events.
helpviewer_keywords: ["ILocation interface [WinLocation]","RegisterForReport method","ILocation.RegisterForReport","ILocation::RegisterForReport","RegisterForReport","RegisterForReport method [WinLocation]","RegisterForReport method [WinLocation]","ILocation interface","WinLocation_COM_Ref.ilocation_registerforreport","locationapi/ILocation::RegisterForReport"]
old-location: winlocation_com_ref\ilocation_registerforreport.htm
tech.root: winlocation
ms.assetid: 1aca3e5b-20cb-4fa9-b28d-7d992601df96
ms.date: 12/05/2018
ms.keywords: ILocation interface [WinLocation],RegisterForReport method, ILocation.RegisterForReport, ILocation::RegisterForReport, RegisterForReport, RegisterForReport method [WinLocation], RegisterForReport method [WinLocation],ILocation interface, WinLocation_COM_Ref.ilocation_registerforreport, locationapi/ILocation::RegisterForReport
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
 - ILocation::RegisterForReport
 - locationapi/ILocation::RegisterForReport
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
 - ILocation.RegisterForReport
---

# ILocation::RegisterForReport


## -description

<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="/uwp/api/windows.devices.geolocation">Windows.Devices.Geolocation</a> API.
]

Requests location report events.

## -parameters

### -param pEvents [in]

Pointer to the <a href="/windows/desktop/api/locationapi/nn-locationapi-ilocationevents">ILocationEvents</a> callback interface through which the requested event notifications will be received.

### -param reportType [in]

<b>GUID</b> that specifies the interface ID of the report type for which to receive event notifications.

### -param dwRequestedReportInterval [in]

<b>DWORD</b> that specifies the requested elapsed time, in milliseconds, between event notifications for the specified report type. If <i>dwRequestedReportInterval</i> is zero, no minimum interval is specified and your application requests to receive events at the location sensor's default interval. See Remarks.

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
<i>reportType </i> is other than IID_ILatLongReport or IID_ICivicAddressReport. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_REGISTERED)</b></dt>
</dl>
</td>
<td width="60%">
<i>reportType </i> is already registered. 

</td>
</tr>
</table>

## -remarks

The interval you request by using the <i>dwRequestedReportInterval</i> parameter represents the shortest amount of time between events. This means that you request to receive event notifications no more frequently than specified, but the elapsed time may be significantly longer. Use the <i>dwRequestedReportInterval</i> parameter to help ensure that event notifications do not use more processor resources than necessary.

The location provider is not required to provide reports at the interval that you request. Call <a href="/windows/desktop/api/locationapi/nf-locationapi-ilocation-getreportinterval">GetReportInterval</a> to discover the true report interval setting.

Applications that need to get location data only once, to fill out a form or place the user's location on a map, should register for events and wait for the first report event as described in <a href="/previous-versions/visualstudio">Waiting For a Location Report</a>.


#### Examples

The following example calls <b>RegisterForReport</b> to subscribe to events.


```cpp
#include <windows.h>
#include <atlbase.h>
#include <atlcom.h>
#include <LocationApi.h> // This is the main Location API header
#include "LocationCallback.h" // This is our callback interface that receives Location reports.

class CInitializeATL : public CAtlExeModuleT<CInitializeATL>{};
CInitializeATL g_InitializeATL; // Initializes ATL for this application. This also does CoInitialize for us

int wmain()
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED | COINIT_DISABLE_OLE1DDE);;
    if (SUCCEEDED(hr))
    {
        CComPtr<ILocation> spLocation; // This is the main Location interface
        CComObject<CLocationEvents>* pLocationEvents = NULL; // This is our callback object for location reports
        IID REPORT_TYPES[] = { IID_ILatLongReport }; // Array of report types of interest. Other ones include IID_ICivicAddressReport

        hr = spLocation.CoCreateInstance(CLSID_Location); // Create the Location object

        if (SUCCEEDED(hr))
        {
            hr = CComObject<CLocationEvents>::CreateInstance(&pLocationEvents); // Create the callback object
            if (NULL != pLocationEvents)
            {
                pLocationEvents->AddRef();
            }
        }

        if (SUCCEEDED(hr))
        {
            // Request permissions for this user account to receive location data for all the
            // types defined in REPORT_TYPES (which is currently just one report)
            if (FAILED(spLocation->RequestPermissions(NULL, REPORT_TYPES, ARRAYSIZE(REPORT_TYPES), FALSE))) // FALSE means an asynchronous request
            {
                wprintf(L"Warning: Unable to request permissions.\n");
            }

            // Tell the Location API that we want to register for reports (which is currently just one report)
            for (DWORD index = 0; index < ARRAYSIZE(REPORT_TYPES); index++)
            {
                hr = spLocation->RegisterForReport(pLocationEvents, REPORT_TYPES[index], 0);
            }
        }

        if (SUCCEEDED(hr))
        {
            // Wait until user presses a key to exit app. During this time the Location API
            // will send reports to our callback interface on another thread.
            system("pause");

            // Unregister from reports from the Location API
            for (DWORD index = 0; index < ARRAYSIZE(REPORT_TYPES); index++)
            {
                spLocation->UnregisterForReport(REPORT_TYPES[index]);
            }
        }

        // Cleanup
        if (NULL != pLocationEvents)
        {
            pLocationEvents->Release();
            pLocationEvents = NULL;
        }

        CoUninitialize();
    }

    return 0;
}

```

## -see-also

<a href="/windows/desktop/api/locationapi/nn-locationapi-ilocation">ILocation</a>



<a href="/windows/desktop/api/locationapi/nn-locationapi-ilocationevents">ILocationEvents</a>