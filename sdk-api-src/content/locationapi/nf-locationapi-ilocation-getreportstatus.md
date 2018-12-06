---
UID: NF:locationapi.ILocation.GetReportStatus
title: ILocation::GetReportStatus
author: windows-sdk-content
description: Retrieves the status for the specified report type.
old-location: winlocation_com_ref\ilocation_getreportstatus.htm
tech.root: locationapi
ms.assetid: 9b7c72cc-fa09-44b2-97be-f200fab7b31d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetReportStatus, GetReportStatus method [WinLocation], GetReportStatus method [WinLocation],ILocation interface, ILocation interface [WinLocation],GetReportStatus method, ILocation.GetReportStatus, ILocation::GetReportStatus, WinLocation_COM_Ref.ilocation_getreportstatus, locationapi/ILocation::GetReportStatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - LocationAPI.dll
api_name:
 - ILocation.GetReportStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILocation::GetReportStatus


## -description


<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/fd40bf4a-c59a-43a4-ab01-c671a8a41731">Windows.Devices.Geolocation</a>API.
]

Retrieves the status for the specified report type. 


## -parameters




### -param reportType [in]

<b>REFIID</b> that specifies the report type for which to get the interval.


### -param arg2 [out]

Address of a <a href="https://msdn.microsoft.com/440e64cb-d09c-47cd-9434-8d4479fa52e2">LOCATION_REPORT_STATUS</a> that receives the current status for the specified report.


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
<i>reportType </i> is other than <b>IID_ILatLongReport</b> or <b>IID_ICivicAddressReport</b>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pStatus</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method retrieves report status for new reports. The most recent reports remain available through <a href="https://msdn.microsoft.com/69d0fed5-7f02-4d74-bdbd-3a0fd85e76ed">ILocation::GetReport</a>, regardless of the status reported by this method.

<h3><a id="Known_Issues"></a><a id="known_issues"></a><a id="KNOWN_ISSUES"></a>Known Issues</h3>
When an application first starts, or when a new location sensor is enabled, <b>GetReportStatus</b> may report a status of <b>REPORT_RUNNING</b>  shortly before the location report is available.

Therefore, an initial call to <a href="https://msdn.microsoft.com/69d0fed5-7f02-4d74-bdbd-3a0fd85e76ed">GetReport</a> will return an error (<b>ERROR_NO_DATA</b>) or a value that is not from the expected location sensor, even if <b>GetReportStatus</b> indicates a status of <b>REPORT_RUNNING</b>. This can happen in the following cases:<ol>
<li>The application polls for status by using <b>GetReportStatus</b> until a report status of <b>REPORT_RUNNING</b> is returned, and then calls <a href="https://msdn.microsoft.com/69d0fed5-7f02-4d74-bdbd-3a0fd85e76ed">GetReport</a>.  </li>
<li><b>GetReportStatus</b> is called when the application starts. This may occur after creation of the location object, or after calling <a href="https://msdn.microsoft.com/eef60203-8705-4f68-be30-c9e7938e5596">RequestPermissions</a>.</li>
</ol>


An application can mitigate the issue by implementing the following workaround. The workaround involves subscribing to location report events.

<h3><a id="Workaround__Subscribing_to_Events"></a><a id="workaround__subscribing_to_events"></a><a id="WORKAROUND__SUBSCRIBING_TO_EVENTS"></a>Workaround: Subscribing to Events</h3>
 The application can subscribe to report events and wait for the report from the <a href="https://msdn.microsoft.com/14353c8e-15f5-493b-9b49-139924f2397e">OnLocationChanged</a> event or the <a href="https://msdn.microsoft.com/d13d8b72-3188-479f-a70c-52b1a9435b80">OnStatusChanged</a> event. The application should wait for a specified finite amount of time.

The following example shows an application that waits for a location report of type <a href="https://msdn.microsoft.com/b489959e-74c7-46df-b63f-7d37e3a244d5">ILatLongReport</a>. If a report is successfully retrieved within the specified amount of time, it prints out a message indicating that data was received.

The following example code demonstrates how an application may call a function named <b>WaitForLocationReport</b> that registers for events and waits for the first location report. <b>WaitForLocationReport</b> waits for an event that is set by a callback object. The function <b>WaitForLocationReport</b> and the callback object is defined in the examples that follow this one.

<div class="code"></div>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// main.cpp
// An application that demonstrates how to wait for a location report.
// This sample waits for latitude/longitude reports but can be modified
// to wait for civic address reports by replacing IID_ILatLongReport 
// with IID_ICivicAddressReport in the following code.

#include "WaitForLocationReport.h"

#define DEFAULT_WAIT_FOR_LOCATION_REPORT 500 // Wait for half a second.

int wmain()
{
    // You may use the flags COINIT_MULTITHREADED | COINIT_DISABLE_OLE1DDE
    // to specify the multi-threaded concurrency model.
    HRESULT hr = ::CoInitializeEx(NULL,
        COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE); 
    if (SUCCEEDED(hr))
    {
        int args;
        PWSTR *pszArgList = ::CommandLineToArgvW(::GetCommandLineW(), &amp;args);

        DWORD const dwTimeToWait = 
            (2 == args) ? static_cast&lt;DWORD&gt;(_wtoi(pszArgList[1])) : DEFAULT_WAIT_FOR_LOCATION_REPORT;

        ::LocalFree(pszArgList);

        wprintf_s(L"Wait time set to %lu\n", dwTimeToWait);

        ILocation *pLocation; // This is the main Location interface.
        hr = CoCreateInstance(CLSID_Location, NULL, CLSCTX_INPROC, IID_PPV_ARGS(&amp;pLocation));
        if (SUCCEEDED(hr))
        {
            // Array of report types to listen for.
            // Replace IID_ILatLongReport with IID_ICivicAddressReport
            // for civic address reports.
            IID REPORT_TYPES[] = { IID_ILatLongReport }; 

            // Request permissions for this user account to receive location data for all the
            // types defined in REPORT_TYPES (which is currently just one report)
            // TRUE means an synchronous request.
            if (FAILED(pLocation-&gt;RequestPermissions(NULL, REPORT_TYPES, ARRAYSIZE(REPORT_TYPES), TRUE))) 
            {
                wprintf_s(L"Warning: Unable to request permissions.\n");
            }

            ILocationReport *pLocationReport; // This is our location report object
            // Replace IID_ILatLongReport with IID_ICivicAddressReport for civic address reports
            hr = ::WaitForLocationReport(pLocation, IID_ILatLongReport, dwTimeToWait, &amp;pLocationReport);
            if (SUCCEEDED(hr))
            {
                wprintf_s(L"Succesfully received data via GetReport().\n");
                pLocationReport-&gt;Release();
            }
            else if (RPC_S_CALLPENDING == hr)
            {
                wprintf_s(L"No LatLong data received.  Wait time of %lu elapsed.\n", dwTimeToWait);
            }
            pLocation-&gt;Release();
        }

        ::CoUninitialize();
    }

    return 0;
}
</pre>
</td>
</tr>
</table></span></div>
The following example code is separated into WaitForLocationReport.h and WaitForLocationReport.cpp. WaitForLocationReport.h contains the header for the <b>WaitForLocationReport</b> function. WaitForLocationReport.cpp contains the definition of the <b>WaitForLocationReport</b> function and the definition of the callback object that it uses. The callback object provides implementations of the <a href="https://msdn.microsoft.com/14353c8e-15f5-493b-9b49-139924f2397e">OnLocationChanged</a> and <a href="https://msdn.microsoft.com/d13d8b72-3188-479f-a70c-52b1a9435b80">OnStatusChanged</a> callback methods. Within these methods, it sets an event that signals when a report is available.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// WaitForLocationReport.h
// Header for the declaration of the WaitForLocationReport function.

#pragma once

#include &lt;windows.h&gt;
#include &lt;LocationApi.h&gt;
#include &lt;wchar.h&gt;

HRESULT WaitForLocationReport(
    ILocation* pLocation,              // Location object.
    REFIID reportType,                 // Type of report.
    DWORD dwTimeToWait,                // Milliseconds to wait.
    ILocationReport** ppLocationReport // Receives the location report.
);
</pre>
</td>
</tr>
</table></span><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// WaitForLocationReport.cpp
// Contains definitions of the WaitForLocationReport function and
// the callback object that it uses.

#include "WaitForLocationReport.h"
#include &lt;shlwapi.h&gt;
#include &lt;new&gt;

// Implementation of the callback interface that receives location reports.
class CLocationCallback : public ILocationEvents
{
public:
    CLocationCallback() : _cRef(1), _hDataEvent(::CreateEvent(
        NULL,  // Default security attributes.
        FALSE, // Auto-reset event.
        FALSE, // Initial state is nonsignaled.
        NULL)) // No event name.
    {
    }

    virtual ~CLocationCallback()
    {
        if (_hDataEvent)
        {
            ::CloseHandle(_hDataEvent);
        }
    }

    IFACEMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        if ((riid == IID_IUnknown) || 
            (riid == IID_ILocationEvents))
        {
            *ppv = static_cast&lt;ILocationEvents*&gt;(this);
        }
        else
        {
            *ppv = NULL;
            return E_NOINTERFACE;
        }
        AddRef();
        return S_OK;
    }

    IFACEMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&amp;_cRef);
    }

    IFACEMETHODIMP_(ULONG) Release()
    {
        long cRef = InterlockedDecrement(&amp;_cRef);
        if (!cRef)
        {
            delete this;
        }
        return cRef;
    }

    // ILocationEvents

    // This is called when there is a new location report.
    IFACEMETHODIMP OnLocationChanged(REFIID /*reportType*/, ILocationReport* /*pLocationReport*/)
    {
        ::SetEvent(_hDataEvent);
        return S_OK;
    }

    // This is called when the status of a report type changes.
    // The LOCATION_REPORT_STATUS enumeration is defined in LocApi.h in the SDK
    IFACEMETHODIMP OnStatusChanged(REFIID /*reportType*/, LOCATION_REPORT_STATUS status)
    {
        if (REPORT_RUNNING == status)
        {
            ::SetEvent(_hDataEvent);
        }
        return S_OK;
    }

    HANDLE GetEventHandle()
    {
        return _hDataEvent;
    }

private:
    long _cRef;
    HANDLE _hDataEvent;    // Data Event Handle
};

// Waits to receive a location report. 
// This function waits for the callback object to signal when
// a report event or status event occurs, and then calls GetReport.
// Even if no report event or status event is received before the timeout,
// this function still queries for the last known report by calling GetReport.
// The last known report may be cached data from a location sensor that is not
// reporting events, or data from the default location provider.
//
// Returns S_OK if the location report has been returned
// or RPC_S_CALLPENDING if the timeout expired.
HRESULT WaitForLocationReport(
    ILocation* pLocation,               // Location object.
    REFIID reportType,                 // Type of report to wait for.
    DWORD dwTimeToWait,                // Milliseconds to wait.
    ILocationReport **ppLocationReport // Receives the location report.
    )
{
    *ppLocationReport = NULL;

    CLocationCallback *pLocationCallback = new(std::nothrow) CLocationCallback();
    HRESULT hr = pLocationCallback ? S_OK : E_OUTOFMEMORY;
    if (SUCCEEDED(hr))
    {
        HANDLE hEvent = pLocationCallback-&gt;GetEventHandle();
        hr = hEvent ? S_OK : E_FAIL;
        if (SUCCEEDED(hr))
        {
            // Tell the Location API that we want to register for a report. 
            hr = pLocation-&gt;RegisterForReport(pLocationCallback, reportType, 0);
            if (SUCCEEDED(hr))
            {
                DWORD dwIndex;
                HRESULT hrWait = CoWaitForMultipleHandles(0, dwTimeToWait, 1, &amp;hEvent, &amp;dwIndex);
                if ((S_OK == hrWait) || (RPC_S_CALLPENDING == hrWait))
                {
                    // Even if there is a timeout indicated by RPC_S_CALLPENDING
                    // attempt to query the report to return the last known report.
                    hr = pLocation-&gt;GetReport(reportType, ppLocationReport);
                    if (FAILED(hr) &amp;&amp; (RPC_S_CALLPENDING == hrWait))
                    {
                        // Override hr error if the request timed out and
                        // no data is available from the last known report.  
                        hr = hrWait;    // RPC_S_CALLPENDING
                    }
                }
                // Unregister from reports from the Location API.
                pLocation-&gt;UnregisterForReport(reportType);
            }
        }
        pLocationCallback-&gt;Release();
    }
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/beeedbbd-df93-4c05-a215-4cfd14e03076">ILocation</a>
 

 

