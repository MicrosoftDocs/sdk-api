---
UID: NE:locationapi.LOCATION_REPORT_STATUS
title: LOCATION_REPORT_STATUS
author: windows-sdk-content
description: Defines possible status for new reports of a particular report type.
old-location: winlocation_com_ref\location_report_status.htm
old-project: locationapi
ms.assetid: 440e64cb-d09c-47cd-9434-8d4479fa52e2
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: LOCATION_REPORT_STATUS, LOCATION_REPORT_STATUS enumeration [WinLocation], REPORT_ACCESS_DENIED, REPORT_ERROR, REPORT_INITIALIZING, REPORT_NOT_SUPPORTED, REPORT_RUNNING, WinLocation_COM_Ref.location_report_status, locationapi/LOCATION_REPORT_STATUS, locationapi/REPORT_ACCESS_DENIED, locationapi/REPORT_ERROR, locationapi/REPORT_INITIALIZING, locationapi/REPORT_NOT_SUPPORTED, locationapi/REPORT_RUNNING
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: locationapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only],Windows 7
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UnloadPerfCounterTextStringsW (Unicode) and UnloadPerfCounterTextStringsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: LOCATION_REPORT_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - LocationApi.h
api_name:
 - LOCATION_REPORT_STATUS
product: Windows
targetos: Windows
req.lib: Loadperf.lib
req.dll: Loadperf.dll
req.irql: 
req.product: GDI+ 1.1
---

# LOCATION_REPORT_STATUS enumeration


## -description


<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/fd40bf4a-c59a-43a4-ab01-c671a8a41731">Windows.Devices.Geolocation</a>
API.
]

Defines possible status for new reports of a particular report type. 


## -enum-fields




### -field REPORT_NOT_SUPPORTED

The requested report type is not supported by the API. No location providers of the requested type are installed.


### -field REPORT_ERROR

There was an error when creating the report, or location providers for the requested type are unable to provide any data. Location providers might be currently unavailable, or location providers cannot obtain any data. For example, this state may occur when a GPS sensor is indoors and no satellites are in view.


### -field REPORT_ACCESS_DENIED

 No permissions have been granted to access this report type. Call <a href="https://msdn.microsoft.com/eef60203-8705-4f68-be30-c9e7938e5596">ILocation::RequestPermissions</a>.


### -field REPORT_INITIALIZING

The report is being initialized.


### -field REPORT_RUNNING

The report is running. New location data for the requested report type is available.


## -remarks



These values represent status for new reports. The most recent reports remain available through <a href="https://msdn.microsoft.com/69d0fed5-7f02-4d74-bdbd-3a0fd85e76ed">ILocation::GetReport</a>, regardless of the reported status. If the status is <b>REPORT_RUNNING</b>, the data in a report is new. Otherwise, <b>ILocation::GetReport</b> provides cached data if cached data is available.


#### Examples

The following code example demonstrates how to retrieve the <b>LOCATION_REPORT_STATUS</b> values from <a href="https://msdn.microsoft.com/9b7c72cc-fa09-44b2-97be-f200fab7b31d">ILocation::GetReportStatus</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    // Get the status of this report type
    if (SUCCEEDED(spLocation-&gt;GetReportStatus(IID_ILatLongReport, &amp;status))) 
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
</pre>
</td>
</tr>
</table></span></div>
The following code is a sample implementation of the callback function <a href="https://msdn.microsoft.com/d13d8b72-3188-479f-a70c-52b1a9435b80">ILocationEvents::OnStatusChanged</a>.  This implementation prints out messages when there is a  change in the status of latitude/longitude reports.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// This is called when the status of a report type changes.
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
</pre>
</td>
</tr>
</table></span></div>


