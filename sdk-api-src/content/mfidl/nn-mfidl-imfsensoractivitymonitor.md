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
The examples below are using [C++/WinRT to author COM callback class](/windows/uwp/cpp-and-winrt-apis/author-coclasses) and [Windows Implementation Libraries (WIL)](https://github.com/Microsoft/wil). 

Full sample Visual Studio project can be found from the [Windows-Camera GitHub repository](https://github.com/microsoft/Windows-Camera)


The following example shows a class declaration that implements  <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivitiesreportcallback">IMFSensorActivitiesReportCallback</a>.


```cpp
class MyCameraNotificationCallback : public winrt::implements <MyCameraNotificationCallback, IMFSensorActivitiesReportCallback>
{
public:
    
    static HRESULT CreateInstance(_In_z_ LPCWSTR symbolicName, _COM_Outptr_ MyCameraNotificationCallback** value) noexcept;

    // IMFSensorActivitiesReportCallback
    IFACEMETHODIMP OnActivitiesReport(_In_ IMFSensorActivitiesReport* sensorActivitiesReport) override;

    bool IsInUse();

private:

    HRESULT Initialize(_In_z_ LPCWSTR symbolicName);

    WCHAR   _symbolicName[MAX_PATH] = {};
    bool    _inUse = false;
    wil::slim_event  _event;
};

```

The next example shows the implementation of the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsensoractivitiesreportcallback-onactivitiesreport">OnActivitiesReport</a> callback.

The OnActivitiesReport function updates a boolean class member to indicate whether the queried sensor device is currently in use and then sets an event to signal that the status has been obtained.

**Note** that the callback can be called multiple times and may not contain any reports, so the event is only set when reports were found.

```cpp

IFACEMETHODIMP MyCameraNotificationCallback::OnActivitiesReport(_In_ IMFSensorActivitiesReport* sensorActivitiesReport)
{
    bool inUse = false;
    wil::com_ptr_nothrow<IMFSensorActivityReport> sensorActivity;
    ULONG cProcCount = 0;

    printf("\nGetActivityReportByDeviceName [%ws] \n", _symbolicName);
    RETURN_IF_FAILED_WITH_EXPECTED(sensorActivitiesReport->GetActivityReportByDeviceName(_symbolicName, &sensorActivity),MF_E_NOT_FOUND);

    RETURN_IF_FAILED(sensorActivity->GetProcessCount(&cProcCount));
    for (ULONG i = 0; i < cProcCount; i++)
    {
        BOOL fStreaming = FALSE;
        wil::com_ptr_nothrow<IMFSensorProcessActivity> processActivity;

        RETURN_IF_FAILED(sensorActivity->GetProcessActivity(i, &processActivity));
        RETURN_IF_FAILED(PrintProcessActivity(processActivity.get()));
        
        RETURN_IF_FAILED(processActivity->GetStreamingState(&fStreaming));

        if (fStreaming)
        {
            inUse = true;
            break;
        }
    }

    // Set flag that the device is in use and then signal event
    _inUse = inUse;
    if (cProcCount > 0)
    {
        _event.SetEvent();
    }

    return S_OK;
}

```


This example shows a class method that waits for the event to be signaled by the <b>OnActivitiesReport</b> callback.
As the OnActivitiesReport will only SetEvent when activities where found, we want to use some reasonable timeout value for WaitForSingleObject, this example uses 500ms and any timeout cases will be translated to "camera not in use".

```cpp
bool MyCameraNotificationCallback::IsInUse( )
{
    if (_event.wait(500))
    {
        return _inUse;
    }

    return false;
}

```


The following example shows an implementation that calls <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatesensoractivitymonitor">MFCreateSensorActivityMonitor</a> to create the activity monitor and then calls the <b>IsInUse</b> class method shown above to determine if the specified sensor is currently in use.

```cpp
HRESULT IsCameraInUse(
    _In_z_ LPCWSTR symbolicName,
    bool& inUse
)
{
    wil::com_ptr_nothrow<MyCameraNotificationCallback> cameraNotificationCallback;
    wil::com_ptr_nothrow<IMFSensorActivityMonitor> activityMonitor;
    wil::com_ptr_nothrow<IMFShutdown> spShutdown;

    RETURN_IF_FAILED(MyCameraNotificationCallback::CreateInstance(symbolicName, &cameraNotificationCallback));

    // Create the IMFSensorActivityMonitor, passing in the IMFSensorActivitiesReportCallback.
    RETURN_IF_FAILED(MFCreateSensorActivityMonitor(cameraNotificationCallback.get(), &activityMonitor));

    // Start the monitor
    RETURN_IF_FAILED(activityMonitor->Start());

    // Call the method that checks to if the monitored device is in use.
    inUse = cameraNotificationCallback->IsInUse();

    // Stop the activity monitor.
    RETURN_IF_FAILED(activityMonitor->Stop());

    // Shutdown the monitor.
    RETURN_IF_FAILED(activityMonitor.query_to(&spShutdown));

    RETURN_IF_FAILED(spShutdown->Shutdown());

    return S_OK;
}

```
