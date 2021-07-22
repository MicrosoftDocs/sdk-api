---
UID: NN:mfidl.IMFSensorActivityMonitor
title: IMFSensorActivityMonitor (mfidl.h)
description: Provides methods for controlling a sensor activity monitor.
helpviewer_keywords: ["IMFSensorActivityMonitor","IMFSensorActivityMonitor interface [Media Foundation]","IMFSensorActivityMonitor interface [Media Foundation]","described","mf.imfsensoractivitymonitor","mfidl/IMFSensorActivityMonitor"]
old-location: mf\imfsensoractivitymonitor.htm
tech.root: mf
ms.assetid: 1D0F8C4E-CB64-4787-A25F-8D826356226C
ms.date: 12/05/2018
ms.keywords: IMFSensorActivityMonitor, IMFSensorActivityMonitor interface [Media Foundation], IMFSensorActivityMonitor interface [Media Foundation],described, mf.imfsensoractivitymonitor, mfidl/IMFSensorActivityMonitor
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
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSensorActivityMonitor
 - mfidl/IMFSensorActivityMonitor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplat.lib
 - mfplat.dll
 - mfplat.dll
 - mfplat.dll.dll
api_name:
 - IMFSensorActivityMonitor
---

# IMFSensorActivityMonitor interface


## -description

Provides methods for controlling a sensor activity monitor.

## -inheritance

The <b>IMFSensorActivityMonitor</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSensorActivityMonitor</b> also has these types of members:

## -remarks

Get an instance of this class by calling <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatesensoractivitymonitor">MFCreateSensorActivityMonitor</a>. Sensor activity reports are delivered through the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivitiesreportcallback">IMFSensorActivitiesReportCallback</a> interface passed into this method.


#### Examples

The following example shows a class declaration that implements  <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivitiesreportcallback">IMFSensorActivitiesReportCallback</a>.


```cpp
class MyCameraNotificationCallback : public RuntimeClass<RuntimeClassFlags<ClassicCom>,
    IMFSensorActivitiesReportCallback,
    FtmBase>
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

```


The next example shows the implementation of the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsensoractivitiesreportcallback-onactivitiesreport">OnActivitiesReport</a> callback that updates a boolean class member to indicate whether the queried sensor device is currently in use and then sets an event to signal that the status has been obtained.


```cpp
IFACEMETHODIMP MyCameraNotificationCallback::OnActivitiesReport(
    _In_ IMFSensorActivitiesReport* sensorActivitiesReport
)
{
    HRESULT hr = S_OK;
    ULONG cCount = 0;
    BOOL inUse = FALSE;
    ComPtr<IMFSensorActivityReport> sensorActivity;

    if (SUCCEEDED(sensorActivitiesReport->GetActivityReportByDeviceName(_symbolicName, &sensorActivity)))
    {
        ULONG cProcCount = 0;

        hr = sensorActivity->GetProcessCount(&cProcCount);
        for (ULONG i = 0; i < cProcCount && SUCCEEDED(hr); i++)
        {
            BOOL fStreaming = FALSE;
            ComPtr<IMFSensorProcessActivity> processActivity;

            hr = sensorActivity->GetProcessActivity(i, &processActivity);
            if (SUCCEEDED(hr))
            {
                hr = processActivity->GetStreamingState(&fStreaming);
            }

            if (SUCCEEDED(hr) && fStreaming)
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

```


This example shows a class method that waits for the event to be signaled by the <b>OnActivitiesReport</b> callback.


```cpp
HRESULT MyCameraNotificationCallback::IsInUse(
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

```


The following example shows an implementation that calls <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatesensoractivitymonitor">MFCreateSensorActivityMonitor</a> to create the activity monitor and then calls the <b>IsInUse</b> class method shown above to determine if the specified sensor is currently in use.


```cpp
HRESULT IsCameraInUse(
    _In_z_ LPCWSTR symbolicName,
    _Out_ BOOL* pfInUse
)
{
    HRESULT hr = S_OK;
    ComPtr<MyCameraNotificationCallback> cameraNotificationCallback;
    ComPtr<IMFSensorActivityMonitor> activityMonitor;
    ComPtr<IMFShutdown> spShutdown;


    MakeAndInitialize<MyCameraNotificationCallback>(&cameraNotificationCallback, symbolicName);

    // Create the IMFSensorActivityMonitor, passing in the IMFSensorActivitiesReportCallback.
    hr = MFCreateSensorActivityMonitor(cameraNotificationCallback.Get(), &activityMonitor);
    if (FAILED(hr))
    {
        return hr;
    }

    // Start the monitor
    hr = activityMonitor->Start();
    if (FAILED(hr))
    {
        return hr;
    }

    // Call the method that checks to if the monitored device is in use.
    cameraNotificationCallback->IsInUse(pfInUse);

    // Stop the activity monitor.
    hr = activityMonitor->Stop();
    if (FAILED(hr))
    {
        return hr;
    }

    // Shutdown the monitor.
    hr = activityMonitor.As(&spShutdown);
    if (FAILED(hr))
    {
        return hr;
    }

    hr = spShutdown->Shutdown();
    if (FAILED(hr))
    {
        return hr;
    }

    return hr;
}

```
