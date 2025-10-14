---
UID: NF:winbio.WinBioAsyncOpenFramework
title: WinBioAsyncOpenFramework function (winbio.h)
description: Opens a handle to the biometric framework. Starting with Windows 10, build 1607, this function is available to use with a mobile image.
helpviewer_keywords: ["WINBIO_ASYNC_NOTIFY_CALLBACK","WINBIO_ASYNC_NOTIFY_MESSAGE","WinBioAsyncOpenFramework","WinBioAsyncOpenFramework function [Windows Biometric Framework API]","secbiomet.winbioasyncopenframework","winbio/WinBioAsyncOpenFramework"]
old-location: secbiomet\winbioasyncopenframework.htm
tech.root: SecBioMet
ms.assetid: D9557A6F-32C4-464F-8800-6E546808F100
ms.date: 12/05/2018
ms.keywords: WINBIO_ASYNC_NOTIFY_CALLBACK, WINBIO_ASYNC_NOTIFY_MESSAGE, WinBioAsyncOpenFramework, WinBioAsyncOpenFramework function [Windows Biometric Framework API], secbiomet.winbioasyncopenframework, winbio/WinBioAsyncOpenFramework
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
 - WinBioAsyncOpenFramework
 - winbio/WinBioAsyncOpenFramework
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
 - WinBioAsyncOpenFramework
---

# WinBioAsyncOpenFramework function


## -description

Opens a handle to the biometric framework. Starting with Windows 10, build 1607, this  function is available to use with a mobile image. You can use this handle to asynchronously enumerate biometric units, databases, and service providers and to receive asynchronous notification when biometric units are attached to the computer or removed.

## -parameters

### -param NotificationMethod [in]

Specifies how completion notifications for asynchronous operations in this framework session are to be delivered to the client application. This must be one of the following values.

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
The framework invokes the callback function defined by the application.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_ASYNC_NOTIFY_MESSAGE"></a><a id="winbio_async_notify_message"></a><dl>
<dt><b>WINBIO_ASYNC_NOTIFY_MESSAGE</b></dt>
</dl>
</td>
<td width="60%">
The framework posts a window message to the application's message queue.

</td>
</tr>
</table>

### -param TargetWindow [in, optional]

Handle  of the window that will receive the completion notices. This value is ignored unless the <i>NotificationMethod</i> parameter is set to <b>WINBIO_ASYNC_NOTIFY_MESSAGE</b>.

### -param MessageCode [in, optional]

Window message code the framework must send to signify completion notices. This value is ignored unless the <i>NotificationMethod</i> parameter is set to <b>WINBIO_ASYNC_NOTIFY_MESSAGE</b>. The value must be within the range <a href="/windows/desktop/winmsg/wm-app">WM_APP</a> (0x8000) to 0xBFFF.

The Windows Biometric Framework sets the <b>LPARAM</b> value of the message to the address of the <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> structure that contains the results of the operation. You must call <a href="/windows/desktop/api/winbio/nf-winbio-winbiofree">WinBioFree</a> to release the structure after you have finished using it.

### -param CallbackRoutine [in, optional]

Address of the callback routine to be invoked for  completion notices. This value is ignored unless the <i>NotificationMethod</i> parameter is set to <b>WINBIO_ASYNC_NOTIFY_CALLBACK</b>.

### -param UserData [in, optional]

Address of a buffer supplied by the caller. The buffer is not modified by the framework or the biometric unit. It is returned in the <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> structure. Your application can use the data to help it determine what actions to perform upon receipt of the completion notice or to maintain additional information about the requested operation.

### -param AsynchronousOpen [in]

Specifies whether to block until the framework session has been opened. Specifying <b>FALSE</b> causes the process to block. Specifying <b>TRUE</b> causes the session to be opened asynchronously.

If you specify <b>FALSE</b> to open the framework session synchronously, success or failure is returned to the caller directly by this function in the  <b>HRESULT</b> return value. If the session is opened successfully, the first  asynchronous completion event your application receives will be for an asynchronous operation requested after the framework has been open.

If you specify <b>TRUE</b> to open the framework session asynchronously, the first asynchronous completion notice received will be for opening the framework. If the <i>NotificationMethod</i> parameter is set to <b>WINBIO_ASYNC_NOTIFY_CALLBACK</b>, operation results are delivered to the <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> structure in the callback function specified by the <i>CallbackRoutine</i> parameter. If the <i>NotificationMethod</i> parameter is set to <b>WINBIO_ASYNC_NOTIFY_MESSAGE</b>, operation results are delivered to the <b>WINBIO_ASYNC_RESULT</b> structure pointed to by the <b>LPARAM</b> field of the window message.

### -param FrameworkHandle [out]

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to create the framework session.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
If you set the notification method to <b>WINBIO_ASYNC_NOTIFY_MESSAGE</b>, the <i>TargetWindow</i> parameter cannot be <b>NULL</b> or <b>HWND_BROADCAST</b> and the <i>MessageCode</i> parameter cannot be zero (0).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>FrameworkHandle</i> parameter and the <i>AsynchronousOpen</i> parameter must be set.

If you set the notification method to <b>WINBIO_ASYNC_NOTIFY_CALLBACK</b>, you must also specify the address of a callback function in the <i>CallbackRoutine</i> parameter.

</td>
</tr>
</table>

## -remarks

The framework handle returned by the <b>WinBioAsyncOpenFramework</b> function can be used to generate asynchronous completion notifications for the following  functions:

<ul>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncenumbiometricunits">WinBioAsyncEnumBiometricUnits</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncenumdatabases">WinBioAsyncEnumDatabases</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncenumserviceproviders">WinBioAsyncEnumServiceProviders</a>
</li>
<li>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncmonitorframeworkchanges">WinBioAsyncMonitorFrameworkChanges</a>
</li>
</ul>
The <i>AsynchronousOpen</i> parameter determines only whether the open operation will block. This parameter has no effect on the completion behavior of subsequent calls that use the session handle.

If you set the  <i>AsynchronousOpen</i> parameter to <b>TRUE</b>, this function will return <b>S_OK</b> as soon as it has performed an initial validation of the arguments. Any errors detected beyond that point will be reported to the caller using the method specified by the <i>NotificationMethod</i> parameter. That is, a successful return value indicates only that the <b>WinBioAsyncOpenFramework</b> parameters were fine and not that the open operation succeeded. To determine whether the open operation succeeded, you must examine the <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> structure.

## -see-also

<a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopensession">WinBioAsyncOpenSession</a>