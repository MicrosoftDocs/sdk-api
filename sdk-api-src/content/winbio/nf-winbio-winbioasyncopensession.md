---
UID: NF:winbio.WinBioAsyncOpenSession
title: WinBioAsyncOpenSession function (winbio.h)
description: Asynchronously connects to a biometric service provider and one or more biometric units. Starting with Windows 10, build 1607, this function is available to use with a mobile image.
helpviewer_keywords: ["WINBIO_ASYNC_NOTIFY_CALLBACK","WINBIO_ASYNC_NOTIFY_MESSAGE","WINBIO_DB_BOOTSTRAP","WINBIO_DB_DEFAULT","WINBIO_DB_ONCHIP","WINBIO_FLAG_ADVANCED","WINBIO_FLAG_BASIC","WINBIO_FLAG_DEFAULT","WINBIO_FLAG_MAINTENANCE","WINBIO_FLAG_RAW","WINBIO_POOL_PRIVATE","WINBIO_POOL_SYSTEM","WinBioAsyncOpenSession","WinBioAsyncOpenSession function [Windows Biometric Framework API]","secbiomet.winbioasyncopensession","winbio/WinBioAsyncOpenSession"]
old-location: secbiomet\winbioasyncopensession.htm
tech.root: SecBioMet
ms.assetid: 711EDE14-A2EE-415D-8FB6-562D71D68146
ms.date: 12/05/2018
ms.keywords: WINBIO_ASYNC_NOTIFY_CALLBACK, WINBIO_ASYNC_NOTIFY_MESSAGE, WINBIO_DB_BOOTSTRAP, WINBIO_DB_DEFAULT, WINBIO_DB_ONCHIP, WINBIO_FLAG_ADVANCED, WINBIO_FLAG_BASIC, WINBIO_FLAG_DEFAULT, WINBIO_FLAG_MAINTENANCE, WINBIO_FLAG_RAW, WINBIO_POOL_PRIVATE, WINBIO_POOL_SYSTEM, WinBioAsyncOpenSession, WinBioAsyncOpenSession function [Windows Biometric Framework API], secbiomet.winbioasyncopensession, winbio/WinBioAsyncOpenSession
req.header: winbio.h
req.include-header: Winbio.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winbio.lib
req.dll: Winbio.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WinBioAsyncOpenSession
 - winbio/WinBioAsyncOpenSession
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-biometrics-winbio-core-l1-1-6.dll
 - ext-ms-win-biometrics-winbio-core-l1-1-5.dll
 - ext-ms-win-biometrics-winbio-core-l1-1-4.dll
 - ext-ms-win-biometrics-winbio-core-l1-1-3.dll
 - ext-ms-win-biometrics-winbio-core-l1-1-2.dll
 - Winbio.dll
 - Ext-MS-Win-BioMetrics-WinBio-Core-l1-1-0.dll
 - Ext-MS-Win-BioMetrics-WinBio-Core-L1-1-1.dll
api_name:
 - WinBioAsyncOpenSession
---

# WinBioAsyncOpenSession function


## -description

Asynchronously connects to a biometric service provider and one or more biometric units. Starting with Windows 10, build 1607, this  function is available to use with a mobile image. If successful, the function returns a biometric session handle. Every operation performed by using this handle will be completed asynchronously, including <a href="/windows/desktop/api/winbio/nf-winbio-winbioclosesession">WinBioCloseSession</a>, and the results will be returned to the client application by using the method specified in the <i>NotificationMethod</i> parameter.

For a synchronous version of this function, see <a href="/windows/desktop/api/winbio/nf-winbio-winbioopensession">WinBioOpenSession</a>.

## -parameters

### -param Factor [in]

A bitmask of <a href="/windows-hardware/drivers/ddi/content/winbio_ioctl/ns-winbio_ioctl-_winbio_sensor_attributes">WINBIO_BIOMETRIC_TYPE</a> flags that specifies the biometric unit types to be enumerated. Only <b>WINBIO_TYPE_FINGERPRINT</b> is currently supported.

### -param PoolType [in]

A <b>ULONG</b> value that specifies the type of the biometric units that will be used in the session. This can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINBIO_POOL_SYSTEM"></a><a id="winbio_pool_system"></a><dl>
<dt><b>WINBIO_POOL_SYSTEM</b></dt>
</dl>
</td>
<td width="60%">
The session connects to a shared collection of biometric units managed by the service provider.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_POOL_PRIVATE"></a><a id="winbio_pool_private"></a><dl>
<dt><b>WINBIO_POOL_PRIVATE</b></dt>
</dl>
</td>
<td width="60%">
The session connects to a collection of biometric units that are managed by the caller.

</td>
</tr>
</table>

### -param Flags [in]

A <b>ULONG</b> value that specifies biometric unit configuration and access characteristics for the new session. Configuration flags specify the general configuration of units in the session. Access flags specify how the application will use the biometric units. You must specify one configuration flag but you can combine that flag with any access flag.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINBIO_FLAG_DEFAULT"></a><a id="winbio_flag_default"></a><dl>
<dt><b>WINBIO_FLAG_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
Group: configuration

The biometric units operate in the manner specified during installation. You must use this value when the <i>PoolType</i> parameter is <b>WINBIO_POOL_SYSTEM</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_FLAG_BASIC"></a><a id="winbio_flag_basic"></a><dl>
<dt><b>WINBIO_FLAG_BASIC</b></dt>
</dl>
</td>
<td width="60%">
Group: configuration

The biometric units operate only as basic capture devices. All processing, matching, and storage operations is performed by software plug-ins.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_FLAG_ADVANCED"></a><a id="winbio_flag_advanced"></a><dl>
<dt><b>WINBIO_FLAG_ADVANCED</b></dt>
</dl>
</td>
<td width="60%">
Group: configuration

The biometric units use internal processing and storage capabilities.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_FLAG_RAW"></a><a id="winbio_flag_raw"></a><dl>
<dt><b>WINBIO_FLAG_RAW</b></dt>
</dl>
</td>
<td width="60%">
Group: access

The client application captures raw biometric data using <a href="/windows/desktop/api/winbio/nf-winbio-winbiocapturesample">WinBioCaptureSample</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_FLAG_MAINTENANCE"></a><a id="winbio_flag_maintenance"></a><dl>
<dt><b>WINBIO_FLAG_MAINTENANCE</b></dt>
</dl>
</td>
<td width="60%">
Group: access

The client performs vendor-defined control operations on a biometric unit by calling <a href="/windows/desktop/api/winbio/nf-winbio-winbiocontrolunitprivileged">WinBioControlUnitPrivileged</a>.

</td>
</tr>
</table>

### -param UnitArray [in, optional]

Pointer to an array of biometric unit identifiers to be included in the session. You can call <a href="/windows/desktop/api/winbio/nf-winbio-winbioenumbiometricunits">WinBioEnumBiometricUnits</a> to enumerate the biometric units. Set this value to <b>NULL</b> if the <i>PoolType</i> parameter is <b>WINBIO_POOL_SYSTEM</b>.

### -param UnitCount [in, optional]

A value that specifies the number of elements in the array pointed to by the <i>UnitArray</i> parameter. Set this value to zero if the <i>PoolType</i> parameter is <b>WINBIO_POOL_SYSTEM</b>.

### -param DatabaseId [in, optional]

A value that specifies the database(s) to be used by the session. If the <i>PoolType</i> parameter is <b>WINBIO_POOL_PRIVATE</b>, you must specify the GUID of an installed database.  If the <i>PoolType</i> parameter is not <b>WINBIO_POOL_PRIVATE</b>, you can specify one of the following common values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINBIO_DB_DEFAULT"></a><a id="winbio_db_default"></a><dl>
<dt><b>WINBIO_DB_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
Each biometric unit in the sensor pool uses the default database specified in the default biometric unit configuration. You must specify this value if the <i>PoolType</i> parameter is <b>WINBIO_POOL_SYSTEM</b>. You cannot use this value if the <i>PoolType</i> parameter is <b>WINBIO_POOL_PRIVATE</b>

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_DB_BOOTSTRAP"></a><a id="winbio_db_bootstrap"></a><dl>
<dt><b>WINBIO_DB_BOOTSTRAP</b></dt>
</dl>
</td>
<td width="60%">
You can specify this value to be used for scenarios prior to starting Windows. Typically, the database is part of the sensor chip or is part of the BIOS and can only be used for template enrollment and deletion.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_DB_ONCHIP"></a><a id="winbio_db_onchip"></a><dl>
<dt><b>WINBIO_DB_ONCHIP</b></dt>
</dl>
</td>
<td width="60%">
The database is on the sensor chip and is available for enrollment and matching.

</td>
</tr>
</table>

### -param NotificationMethod [in]

Specifies how completion notifications for asynchronous operations in this biometric session are to be delivered to the client application. This must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINBIO_ASYNC_NOTIFY_CALLBACK"></a><a id="winbio_async_notify_callback"></a><dl>
<dt><b>WINBIO_ASYNC_NOTIFY_CALLBACK</b></dt>
</dl>
</td>
<td width="60%">
The session invokes the callback function defined by the application.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_ASYNC_NOTIFY_MESSAGE"></a><a id="winbio_async_notify_message"></a><dl>
<dt><b>WINBIO_ASYNC_NOTIFY_MESSAGE</b></dt>
</dl>
</td>
<td width="60%">
The session posts a window message to the application's message queue.

</td>
</tr>
</table>

### -param TargetWindow [in, optional]

Handle  of the window that will receive the completion notices. This value is ignored unless the <i>NotificationMethod</i> parameter is set to <b>WINBIO_ASYNC_NOTIFY_MESSAGE</b>.

### -param MessageCode [in, optional]

Window message code the framework must send to signify completion notices. This value is ignored unless the <i>NotificationMethod</i> parameter is set to <b>WINBIO_ASYNC_NOTIFY_MESSAGE</b>. The value must be within the range WM_APP(0x8000) to 0xBFFF.

The Windows Biometric Framework sets the <b>LPARAM</b> value of the message to the address of the <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> structure that contains the results of the operation. You must call <a href="/windows/desktop/api/winbio/nf-winbio-winbiofree">WinBioFree</a> to release the structure after you have finished using it.

### -param CallbackRoutine [in, optional]

Address of callback routine to be invoked when the operation started by using the session handle completes. This value is ignored unless the  <i>NotificationMethod</i> parameter is set to <b>WINBIO_ASYNC_NOTIFY_CALLBACK</b>.

### -param UserData [in, optional]

Address of a buffer supplied by the caller. The buffer is not modified by the framework or the biometric unit. It is returned in the <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> structure. Your application can use the data to help it determine what actions to perform upon receipt of the completion notice or to maintain additional information about the requested operation.

### -param AsynchronousOpen [in]

Specifies whether to block until the framework session has been opened. Specifying <b>FALSE</b> causes the process to block. Specifying <b>TRUE</b> causes the session to be opened asynchronously.

If you specify <b>FALSE</b> to open the framework session synchronously, success or failure is returned to the caller directly by this function in the  <b>HRESULT</b> return value. If the session is opened successfully, the first  asynchronous completion event your application receives will be for an asynchronous operation requested after the framework has been open.

If you specify <b>TRUE</b> to open the framework session asynchronously, the first asynchronous completion notice received will be for opening the framework. If the <i>NotificationMethod</i> parameter is set to <b>WINBIO_ASYNC_NOTIFY_CALLBACK</b>, operation results are delivered to the <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> structure in the callback function specified by the <i>CallbackRoutine</i> parameter. If the <i>NotificationMethod</i> parameter is set to <b>WINBIO_ASYNC_NOTIFY_MESSAGE</b>, operation results are delivered to the <b>WINBIO_ASYNC_RESULT</b> structure pointed to by the LPARAM field of the window message.

### -param SessionHandle [out, optional]

If the function does not succeed, this parameter will be <b>NULL</b>.

If the session is opened synchronously and successfully, this parameter will contain a pointer to the  session handle.

If you specify that the session be opened asynchronously, this method returns immediately, the session handle will be <b>NULL</b>, and you must examine the <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> structure to determine whether the session was successfully opened.

## -returns

If the function succeeds, it returns <b>S_OK</b>. If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_OUTOFMEMORY</b></b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to create the biometric session.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_INVALIDARG</b></b></dt>
</dl>
</td>
<td width="60%">
If you set the notification method to <b>WINBIO_ASYNC_NOTIFY_MESSAGE</b>, the <i>TargetWindow</i> parameter cannot be <b>NULL</b> or <b>HWND_BROADCAST</b> and the <i>MessageCode</i> parameter cannot be zero (0).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_POINTER</b></b></dt>
</dl>
</td>
<td width="60%">
The <i>SessionHandle</i> parameter and the <i>AsynchronousOpen</i> parameter must be set.

If you set the notification method to <b>WINBIO_ASYNC_NOTIFY_CALLBACK</b>, you must also specify the address of a callback function in the <i>CallbackRoutine</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_ACCESSDENIED</b></b></dt>
</dl>
</td>
<td width="60%">
The <i>Flags</i> parameter contains the <b>WINBIO_FLAG_RAW</b> or the <b>WINBIO_FLAG_MAINTENANCE</b> flag and the caller has not been granted either access permission.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>WINBIO_E_INVALID_UNIT</b></b></dt>
</dl>
</td>
<td width="60%">
One or more of the biometric unit numbers specified in the <i>UnitArray</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>WINBIO_E_NOT_ACTIVE_CONSOLE</b></b></dt>
</dl>
</td>
<td width="60%">
The client application is running on a remote desktop client and is attempting to open a system pool session.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>WINBIO_E_SENSOR_UNAVAILABLE</b></b></dt>
</dl>
</td>
<td width="60%">
The <i>PoolType</i> parameter is set to <b>WINBIO_POOL_PRIVATE</b> and one or more of the requested sensors in that pool is not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>WINBIO_E_DISABLED</b></b></dt>
</dl>
</td>
<td width="60%">
Current administrative policy prohibits use of the Windows Biometric Framework API.

</td>
</tr>
</table>

## -remarks

The session handle returned by the <b>WinBioAsyncOpenSession</b> function can be used to generate asynchronous completion notifications for any of the following functions:

<ul>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbiocancel">WinBioCancel</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbiocapturesample">WinBioCaptureSample</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioclosesession">WinBioCloseSession</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbiocontrolunit">WinBioControlUnit</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbiocontrolunitprivileged">WinBioControlUnitPrivileged</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbiodeletetemplate">WinBioDeleteTemplate</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioenrollbegin">WinBioEnrollBegin</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioenrollcapture">WinBioEnrollCapture</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioenrollcommit">WinBioEnrollCommit</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioenrolldiscard">WinBioEnrollDiscard</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioenumenrollments">WinBioEnumEnrollments</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbiogetproperty">WinBioGetProperty</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioidentify">WinBioIdentify</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbiolocatesensor">WinBioLocateSensor</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbiolockunit">WinBioLockUnit</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbiologonidentifieduser">WinBioLogonIdentifiedUser</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioregistereventmonitor">WinBioRegisterEventMonitor</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbiounlockunit">WinBioUnlockUnit</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbiounregistereventmonitor">WinBioUnregisterEventMonitor</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioverify">WinBioVerify</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbiowait">WinBioWait</a>
</li>
</ul>
The session handle returned by <b>WinBioAsyncOpenSession</b> cannot be used with the following functions:

<ul>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbiocapturesamplewithcallback">WinBioCaptureSampleWithCallback</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioenrollcapturewithcallback">WinBioEnrollCaptureWithCallback</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioidentifywithcallback">WinBioIdentifyWithCallback</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioidentifywithcallback">WinBioIdentifyWithCallback</a>
</li>
</ul>
These functions, first available in Windows 7, have an incompatible callback signature, and their use in new applications is discouraged. Developers who want asynchronous callbacks should instead use <b>WinBioAsyncOpenSession</b> with a <i>NotificationMethod</i> of <b>WINBIO_ASYNC_NOTIFY_CALLBACK</b>.

The <i>AsynchronousOpen</i> parameter determines only whether the open operation will block. This parameter has no effect on the completion behavior of subsequent calls that use the session handle.

If you set the  <i>AsynchronousOpen</i> parameter to <b>TRUE</b>, this function will return <b>S_OK</b> as soon as it has performed an initial validation of the arguments. Any errors detected beyond that point will be reported to the caller using the method specified by the <i>NotificationMethod</i> parameter. That is, a successful return value indicates only that the <b>WinBioAsyncOpenSession</b> parameters were fine and not that the open operation succeeded. To determine whether the open operation succeeded, you must examine the <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> structure.

## -see-also

<a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopenframework">WinBioAsyncOpenFramework</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbioclosesession">WinBioCloseSession</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbioopensession">WinBioOpenSession</a>