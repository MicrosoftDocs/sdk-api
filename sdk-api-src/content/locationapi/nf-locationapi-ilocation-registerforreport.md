---
UID: NF:locationapi.ILocation.RegisterForReport
title: ILocation::RegisterForReport
author: windows-sdk-content
description: Requests location report events.
old-location: winlocation_com_ref\ilocation_registerforreport.htm
tech.root: locationapi
ms.assetid: 1aca3e5b-20cb-4fa9-b28d-7d992601df96
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ILocation interface [WinLocation],RegisterForReport method, ILocation.RegisterForReport, ILocation::RegisterForReport, RegisterForReport, RegisterForReport method [WinLocation], RegisterForReport method [WinLocation],ILocation interface, WinLocation_COM_Ref.ilocation_registerforreport, locationapi/ILocation::RegisterForReport
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
 - ILocation.RegisterForReport
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILocation::RegisterForReport


## -description


<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/fd40bf4a-c59a-43a4-ab01-c671a8a41731">Windows.Devices.Geolocation</a>API.
]

Requests location report events.


## -parameters




### -param pEvents [in]

Pointer to the <a href="https://msdn.microsoft.com/5281ae0f-8599-4f84-a3f3-cde8c69e893d">ILocationEvents</a> callback interface through which the requested event notifications will be received. 


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

The location provider is not required to provide reports at the interval that you request. Call <a href="https://msdn.microsoft.com/c7bcd665-317c-428a-aa20-0d09c8d7a813">GetReportInterval</a> to discover the true report interval setting.

Applications that need to get location data only once, to fill out a form or place the user's location on a map, should register for events and wait for the first report event as described in <a href="https://msdn.microsoft.com/37485532-04f4-4d31-92a4-90545b12e59c">Waiting For a Location Report</a>.


#### Examples

The following example calls <b>RegisterForReport</b> to subscribe to events.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;atlbase.h&gt;
#include &lt;atlcom.h&gt;
#include &lt;LocationApi.h&gt; // This is the main Location API header
#include "LocationCallback.h" // This is our callback interface that receives Location reports.

class CInitializeATL : public CAtlExeModuleT&lt;CInitializeATL&gt;{};
CInitializeATL g_InitializeATL; // Initializes ATL for this application. This also does CoInitialize for us

int wmain()
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED | COINIT_DISABLE_OLE1DDE);;
    if (SUCCEEDED(hr))
    {
        CComPtr&lt;ILocation&gt; spLocation; // This is the main Location interface
        CComObject&lt;CLocationEvents&gt;* pLocationEvents = NULL; // This is our callback object for location reports
        IID REPORT_TYPES[] = { IID_ILatLongReport }; // Array of report types of interest. Other ones include IID_ICivicAddressReport

        hr = spLocation.CoCreateInstance(CLSID_Location); // Create the Location object

        if (SUCCEEDED(hr))
        {
            hr = CComObject&lt;CLocationEvents&gt;::CreateInstance(&amp;pLocationEvents); // Create the callback object
            if (NULL != pLocationEvents)
            {
                pLocationEvents-&gt;AddRef();
            }
        }

        if (SUCCEEDED(hr))
        {
            // Request permissions for this user account to receive location data for all the
            // types defined in REPORT_TYPES (which is currently just one report)
            if (FAILED(spLocation-&gt;RequestPermissions(NULL, REPORT_TYPES, ARRAYSIZE(REPORT_TYPES), FALSE))) // FALSE means an asynchronous request
            {
                wprintf(L"Warning: Unable to request permissions.\n");
            }

            // Tell the Location API that we want to register for reports (which is currently just one report)
            for (DWORD index = 0; index &lt; ARRAYSIZE(REPORT_TYPES); index++)
            {
                hr = spLocation-&gt;RegisterForReport(pLocationEvents, REPORT_TYPES[index], 0);
            }
        }

        if (SUCCEEDED(hr))
        {
            // Wait until user presses a key to exit app. During this time the Location API
            // will send reports to our callback interface on another thread.
            system("pause");

            // Unregister from reports from the Location API
            for (DWORD index = 0; index &lt; ARRAYSIZE(REPORT_TYPES); index++)
            {
                spLocation-&gt;UnregisterForReport(REPORT_TYPES[index]);
            }
        }

        // Cleanup
        if (NULL != pLocationEvents)
        {
            pLocationEvents-&gt;Release();
            pLocationEvents = NULL;
        }

        CoUninitialize();
    }

    return 0;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/beeedbbd-df93-4c05-a215-4cfd14e03076">ILocation</a>



<a href="https://msdn.microsoft.com/5281ae0f-8599-4f84-a3f3-cde8c69e893d">ILocationEvents</a>
 

 

