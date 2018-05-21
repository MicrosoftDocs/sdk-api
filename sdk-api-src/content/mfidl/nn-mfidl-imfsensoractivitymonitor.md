---
UID: NN:mfidl.IMFSensorActivityMonitor
title: IMFSensorActivityMonitor
author: windows-driver-content
description: Provides methods for controlling a sensor activity monitor.
old-location: mf\imfsensoractivitymonitor.htm
old-project: medfound
ms.assetid: 1D0F8C4E-CB64-4787-A25F-8D826356226C
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: IMFSensorActivityMonitor, IMFSensorActivityMonitor interface [Media Foundation], IMFSensorActivityMonitor interface [Media Foundation],described, mf.imfsensoractivitymonitor, mfidl/IMFSensorActivityMonitor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
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
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfplat.lib
-	mfplat.dll
-	mfplat.dll
-	mfplat.dll.dll
api_name:
-	IMFSensorActivityMonitor
product: Windows
targetos: Windows
req.lib: Mfplat.lib; Mfplat.dll
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFSensorActivityMonitor interface


## -description


Provides methods for controlling a sensor activity monitor.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSensorActivityMonitor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFSensorActivityMonitor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSensorActivityMonitor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh973223">Start</a>
</td>
<td align="left" width="63%">
Starts the sensor activity monitor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927275">Stop</a>
</td>
<td align="left" width="63%">
Stops the sensor activity monitor.

</td>
</tr>
</table> 


## -remarks



Get an instance of this class by calling <a href="https://msdn.microsoft.com/852395EE-AA84-4C61-A55F-E8D925FA1447">MFCreateSensorActivityMonitor</a>. Sensor activity reports are delivered through the <a href="https://msdn.microsoft.com/477B008D-7F0A-4084-BDFD-DF19E2A82817">IMFSensorActivitiesReportCallback</a> interface passed into this method.


#### Examples

The following example shows a class declaration that implements  <a href="https://msdn.microsoft.com/477B008D-7F0A-4084-BDFD-DF19E2A82817">IMFSensorActivitiesReportCallback</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>class MyCameraNotificationCallback : public RuntimeClass&lt;RuntimeClassFlags&lt;ClassicCom&gt;,
    IMFSensorActivitiesReportCallback,
    FtmBase&gt;
{
public:
    MyCameraNotificationCallback() {};
    //MyCameraNotificationCallback();
    virtual ~MyCameraNotificationCallback();

    HRESULT RuntimeClassInitialize(_In_z_ LPCWSTR SymbolicName)
    {
        return wcscpy_s(_symbolicName, SymbolicName);
    }

    // IMFSensorActivitiesReportCallback
    IFACEMETHOD(OnActivitiesReport)(_In_ IMFSensorActivitiesReport* sensorActivitiesReport) override;

    HRESULT IsInUse(_Out_ BOOL* pinUse);

private:

    WCHAR _symbolicName[MAX_PATH];
    BOOL _inUse;
    HANDLE _hEvent;
    HRESULT _hrStatus;
};
</pre>
</td>
</tr>
</table></span></div>
The next example shows the implementation of the <a href="https://msdn.microsoft.com/B4D2332C-757F-4A2A-A12B-81BB503B02A4">OnActivitiesReport</a> callback that updates a boolean class member to indicate whether the queried sensor device is currently in use and then sets an event to signal that the status has been obtained.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IFACEMETHODIMP MyCameraNotificationCallback::OnActivitiesReport(
    _In_ IMFSensorActivitiesReport* sensorActivitiesReport
)
{
    HRESULT hr = S_OK;
    ULONG cCount = 0;
    BOOL inUse = FALSE;
    ComPtr&lt;IMFSensorActivityReport&gt; sensorActivity;

    if (SUCCEEDED(sensorActivitiesReport-&gt;GetActivityReportByDeviceName(_symbolicName, &amp;sensorActivity)))
    {
        ULONG cProcCount = 0;

        hr = sensorActivity-&gt;GetProcessCount(&amp;cProcCount);
        for (ULONG i = 0; i &lt; cProcCount &amp;&amp; SUCCEEDED(hr); i++)
        {
            BOOL fStreaming = FALSE;
            ComPtr&lt;IMFSensorProcessActivity&gt; processActivity;

            hr = sensorActivity-&gt;GetProcessActivity(i, &amp;processActivity);
            if (SUCCEEDED(hr))
            {
                hr = processActivity-&gt;GetStreamingState(&amp;fStreaming);
            }

            if (SUCCEEDED(hr) &amp;&amp; fStreaming)
            {
                inUse = TRUE;
                break;
            }
        }
    }

    // Set flag that the device is in use and then signal event
    _inUse = inUse;
    _hrStatus = hr;
    SetEvent(_hEvent);

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>
This example shows a class method that waits for the event to be signaled by the <b>OnActivitiesReport</b> callback.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT MyCameraNotificationCallback::IsInUse(
    _Out_ BOOL* pfInUse
)
{
    HRESULT hr = S_OK;
    DWORD   dwWait = 0;

    *pfInUse = FALSE;

    dwWait = WaitForSingleObject(_hEvent, INFINITE);
    switch (dwWait)
    {
    case WAIT_OBJECT_0:
        *pfInUse = _inUse;
        hr = _hrStatus;
        break;
    case WAIT_TIMEOUT:
    case WAIT_ABANDONED:
        hr = MF_E_UNEXPECTED;
        break;
    case WAIT_FAILED:
    default:
        hr = HRESULT_FROM_WIN32(GetLastError());
        break;
    }

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>
The following example shows an implementation that calls <a href="https://msdn.microsoft.com/852395EE-AA84-4C61-A55F-E8D925FA1447">MFCreateSensorActivityMonitor</a> to create the activity monitor and then calls the <b>IsInUse</b> class method shown above to determine if the specified sensor is currently in use.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT IsCameraInUse(
    _In_z_ LPCWSTR symbolicName,
    _Out_ BOOL* pfInUse
)
{
    HRESULT hr = S_OK;
    ComPtr&lt;MyCameraNotificationCallback&gt; cameraNotificationCallback;
    ComPtr&lt;IMFSensorActivityMonitor&gt; activityMonitor;
    ComPtr&lt;IMFShutdown&gt; spShutdown;


    MakeAndInitialize&lt;MyCameraNotificationCallback&gt;(&amp;cameraNotificationCallback, symbolicName);

    // Create the IMFSensorActivityMonitor, passing in the IMFSensorActivitiesReportCallback.
    hr = MFCreateSensorActivityMonitor(cameraNotificationCallback.Get(), &amp;activityMonitor);
    if (FAILED(hr))
    {
        return hr;
    }

    // Start the monitor
    hr = activityMonitor-&gt;Start();
    if (FAILED(hr))
    {
        return hr;
    }

    // Call the method that checks to if the monitored device is in use.
    cameraNotificationCallback-&gt;IsInUse(pfInUse);

    // Stop the activity monitor.
    hr = activityMonitor-&gt;Stop();
    if (FAILED(hr))
    {
        return hr;
    }

    // Shutdown the monitor.
    hr = activityMonitor.As(&amp;spShutdown);
    if (FAILED(hr))
    {
        return hr;
    }

    hr = spShutdown-&gt;Shutdown();
    if (FAILED(hr))
    {
        return hr;
    }

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>


