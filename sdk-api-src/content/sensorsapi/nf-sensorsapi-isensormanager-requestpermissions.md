---
UID: NF:sensorsapi.ISensorManager.RequestPermissions
title: ISensorManager::RequestPermissions (sensorsapi.h)
description: Opens a system dialog box to request user permission to access sensor data.
helpviewer_keywords: ["FALSE","ISensorManager interface","RequestPermissions method","ISensorManager.RequestPermissions","ISensorManager::RequestPermissions","RequestPermissions","RequestPermissions method","RequestPermissions method","ISensorManager interface","TRUE","sensorsapi/ISensorManager::RequestPermissions","winsensors_com_ref.Isensormanager_requestpermissions"]
old-location: winsensors_com_ref\Isensormanager_requestpermissions.htm
tech.root: winsensors
ms.assetid: 6a21820c-4f13-4220-ad13-34d0226597b6
ms.date: 09/19/2025
ms.keywords: FALSE, ISensorManager interface,RequestPermissions method, ISensorManager.RequestPermissions, ISensorManager::RequestPermissions, RequestPermissions, RequestPermissions method, RequestPermissions method,ISensorManager interface, TRUE, sensorsapi/ISensorManager::RequestPermissions, winsensors_com_ref.Isensormanager_requestpermissions
req.header: sensorsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
req.lib: Sensorsapi.lib
req.dll: Sensorsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISensorManager::RequestPermissions
 - sensorsapi/ISensorManager::RequestPermissions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sensorsapi.dll
api_name:
 - ISensorManager.RequestPermissions
---

# ISensorManager::RequestPermissions


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

Opens a system dialog box to request user permission to access sensor data.

## -parameters

### -param hParent [in]

For Windows 8, if <i>hParent</i> is provided a value, then the dialog will be modal to the parent window. If <i>hParent</i> is <b>NULL</b>, then the dialog will not be modal.  The dialog is always synchronous.

For Windows 7, <b>HWND</b> is handle to a window that can act as a parent to the permissions dialog box. Must be <b>NULL</b> if <i>fModal</i> is <b>TRUE</b>.

### -param pSensors [in]

For Windows 8, this value is not used.

For Windows 7, <i>pSensors</i> is a pointer to the <a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorcollection">ISensorCollection</a> interface that contains the list of sensors for which permission is being requested.

### -param fModal [in]

For Windows 8, this value is not used. Refer to <i>hParent</i> for control of modality.

For Windows 7, <i>fModal</i> is a <b>BOOL</b> that specifies the dialog box mode. Must be <b>FALSE</b> if <i>hParent</i> is non-null.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
If <i>hParent</i> is <b>NULL</b>, the dialog box is modal and therefore has exclusive focus in Windows until the user responds. The call is synchronous. The return code indicates the user choice. See Return Value. 

If <i>hParent</i> is non-null, the call is asynchronous and the calling thread will not wait for the dialog box to be closed. The return code indicates whether the call succeeded. See Return Value.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The dialog box is modeless. The call is asynchronous and the calling thread will not wait for the dialog box to be closed. The return code indicates whether the call succeeded. See Return Value.

The <i>hParent</i> parameter is ignored.

</td>
</tr>
</table>

## -returns

The following table describes return codes for  synchronous results.

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
The user enabled the sensors.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)</b></dt>
</dl>
</td>
<td width="60%">
The user chose to disable the sensors. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_CANCELLED) </b></dt>
</dl>
</td>
<td width="60%">
The user canceled the dialog box or refused elevation of permission to show the dialog box.

</td>
</tr>
</table>
 

The following table describes return codes for  asynchronous results.

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
All of the sensors in the sensor collection were displayed for the user to enable. The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Some of the sensors in the sensor collection were displayed for the user to enable. Some sensors may have been removed from the collection; for example, because the user had previously chosen to keep them disabled. The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An argument is  not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A pointer is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)</b></dt>
</dl>
</td>
<td width="60%">
All sensors in the sensor collection were previously disabled by the user. The dialog box was not shown.

</td>
</tr>
</table>

## -remarks

Making a synchronous call from the user interface (UI) thread of a Windows application can block the UI thread and make the application less responsive. To prevent this, do not call this method from the UI thread with <i>fModal</i> set to <b>TRUE</b>.

<div class="alert"><b>Note</b>  <p class="note">If an application or plugin that is running in protected mode, such as a Browser Helper Object (BHO) for Internet Explorer when Internet Explorer is running in protected mode, calls <b>RequestPermissions</b>, and the user chooses the <b>Don't enable this location sensor</b> option in the dialog box, Windows will display the dialog box again if <b>RequestPermissions</b> is called again by the same user. Applications that run in protected mode may choose to avoid calling <b>RequestPermissions</b> on startup so that the user will not be subjected to a possible unwanted dialog box each time the application starts.

</div>
<div> </div>

#### Examples

The following example code requests permissions for all sensors retrieved from the sensor manager, by type, using an asynchronous method call. The platform will only prompt the user to enable sensors that are not already enabled. To determine whether the user enabled any sensors in this case, you must handle the <a href="/windows/desktop/api/sensorsapi/nf-sensorsapi-isensorevents-onstatechanged">ISensorEvents::OnStateChanged</a> event. For additional examples that demonstrate how to request permissions, see <a href="/windows/desktop/SensorsAPI/requesting-user-permissions">Requesting User Permissions</a>.


```cpp
// Get the sensor collection.
hr = pSensorManager->GetSensorsByType(SAMPLE_SENSOR_TYPE_TIME, &pSensorColl);

if(SUCCEEDED(hr))
{
    // Request permissions for all sensors
    // in the collection.
    hr = pSensorManager->RequestPermissions(0, pSensorColl, FALSE);
}


```

## -see-also

<a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager">ISensorManager</a>



<a href="/windows/desktop/SensorsAPI/managing-user-permissions">Managing User Permissions</a>



<a href="/windows/desktop/SensorsAPI/requesting-user-permissions">Requesting User Permissions</a>