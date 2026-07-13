---
UID: NF:winbio.WinBioControlUnit
title: WinBioControlUnit function (winbio.h)
description: Allows the caller to perform vendor-defined control operations on a biometric unit. Starting with Windows 10, build 1607, this function is available to use with a mobile image.
helpviewer_keywords: ["WINBIO_COMPONENT_ENGINE","WINBIO_COMPONENT_SENSOR","WINBIO_COMPONENT_STORAGE","WinBioControlUnit","WinBioControlUnit function [Windows Biometric Framework API]","secbiomet.winbiocontrolunit","winbio/WinBioControlUnit"]
old-location: secbiomet\winbiocontrolunit.htm
tech.root: SecBioMet
ms.assetid: 5d11f72a-3392-4089-a563-1771f8c2c8f7
ms.date: 12/05/2018
ms.keywords: WINBIO_COMPONENT_ENGINE, WINBIO_COMPONENT_SENSOR, WINBIO_COMPONENT_STORAGE, WinBioControlUnit, WinBioControlUnit function [Windows Biometric Framework API], secbiomet.winbiocontrolunit, winbio/WinBioControlUnit
req.header: winbio.h
req.include-header: Winbio.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - WinBioControlUnit
 - winbio/WinBioControlUnit
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
 - Ext-MS-Win-BioMetrics-WinBio-l1-2-0.dll
 - winbioext.dll
 - Ext-MS-Win-BioMetrics-WinBio-Core-L1-1-0.dll
 - Ext-MS-Win-BioMetrics-WinBio-Core-L1-1-1.dll
api_name:
 - WinBioControlUnit
---

# WinBioControlUnit function


## -description

Allows the caller to perform vendor-defined control operations on a biometric unit. Starting with Windows 10, build 1607, this  function is available to use with a mobile image. This function is provided for access to extended vendor operations for which elevated privileges are not required. If access rights are required, call the <a href="/windows/desktop/api/winbio/nf-winbio-winbiocontrolunitprivileged">WinBioControlUnitPrivileged</a> function.

## -parameters

### -param SessionHandle [in]

A <b>WINBIO_SESSION_HANDLE</b> value that identifies an open biometric session. Open a synchronous session handle by calling <a href="/windows/desktop/api/winbio/nf-winbio-winbioopensession">WinBioOpenSession</a>. Open an asynchronous session handle by calling <a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopensession">WinBioAsyncOpenSession</a>.

### -param UnitId [in]

A <b>WINBIO_UNIT_ID</b> value that identifies the biometric unit. This value must correspond to the unit ID used previously in  the <a href="/windows/desktop/api/winbio/nf-winbio-winbiolockunit">WinBioLockUnit</a> function.

### -param Component [in]

A <b>WINBIO_COMPONENT</b> value that specifies the component within the biometric unit that should perform the operation. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINBIO_COMPONENT_SENSOR"></a><a id="winbio_component_sensor"></a><dl>
<dt><b>WINBIO_COMPONENT_SENSOR</b></dt>
</dl>
</td>
<td width="60%">
Send the command to the sensor adapter.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_COMPONENT_ENGINE"></a><a id="winbio_component_engine"></a><dl>
<dt><b>WINBIO_COMPONENT_ENGINE</b></dt>
</dl>
</td>
<td width="60%">
Send the command to the engine adapter.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_COMPONENT_STORAGE"></a><a id="winbio_component_storage"></a><dl>
<dt><b>WINBIO_COMPONENT_STORAGE</b></dt>
</dl>
</td>
<td width="60%">
Send the command to the storage adapter.

</td>
</tr>
</table>

### -param ControlCode [in]

A vendor-defined code recognized by the biometric unit specified by the <i>UnitId</i> parameter and the adapter specified by the <i>Component</i> parameter.

### -param SendBuffer

Address of the buffer that contains the control information to be sent to the adapter specified by the <i>Component</i> parameter. The format and content of the buffer is vendor-defined.

### -param SendBufferSize [in]

Size, in bytes, of the buffer specified by the <i>SendBuffer</i> parameter.

### -param ReceiveBuffer

Address of the buffer that receives information sent by the adapter specified by the <i>Component</i> parameter. The format and content of the buffer is vendor-defined.

### -param ReceiveBufferSize [in]

Size, in bytes, of the buffer specified by the <i>ReceiveBuffer</i> parameter.

### -param ReceiveDataSize

Pointer to a <b>SIZE_T</b> value that contains the size, in bytes, of the data written to the buffer specified by the <i>ReceiveBuffer</i> parameter.

### -param OperationStatus [out, optional]

Pointer to an integer that contains a vendor-defined status code that specifies the outcome of the control operation.

## -returns

If the function succeeds, it returns S_OK. If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The session handle is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value specified in the <i>ControlCode</i> parameter is not recognized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>SendBuffer</i>, <i>ReceiveBuffer</i>, <i>ReceiveDataSize</i>, <i>OperationStatus</i> parameters cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_INVALID_CONTROL_CODE</b></dt>
</dl>
</td>
<td width="60%">
The value specified in the <i>ControlCode</i> parameter is not recognized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_LOCK_VIOLATION</b></dt>
</dl>
</td>
<td width="60%">
The biometric unit specified by the <i>UnitId</i> parameter must be locked before any control operations can be performed.

</td>
</tr>
</table>

## -remarks

You must call <a href="/windows/desktop/api/winbio/nf-winbio-winbiolockunit">WinBioLockUnit</a> before calling <b>WinBioControlUnit</b>. The <b>WinBioLockUnit</b> function creates a locked region in which vendor-defined operations can be securely performed.

Vendors who create plug-ins must decide which extended operations are privileged and which are available to all clients. To perform a privileged operation, the client application must call the <a href="/windows/desktop/api/winbio/nf-winbio-winbiocontrolunitprivileged">WinBioControlUnitPrivileged</a> function. The Windows Biometric Framework allows only clients that have the appropriate access rights to call <b>WinBioControlUnitPrivileged</b>.

To use <b>WinBioControlUnit</b> synchronously, call the function with a session handle created by calling <a href="/windows/desktop/api/winbio/nf-winbio-winbioopensession">WinBioOpenSession</a>. The function blocks until the operation completes or an error is encountered.

To use <b>WinBioControlUnit</b> asynchronously, call the function with a session handle created by calling <a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopensession">WinBioAsyncOpenSession</a>. The framework allocates a <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> structure  and uses it to return information about operation success or failure. The <b>WINBIO_ASYNC_RESULT</b> structure is returned to the application callback or to the application message queue, depending on the value you set in the <i>NotificationMethod</i> parameter of the <b>WinBioAsyncOpenSession</b> function.

<ul>
<li>If you choose to receive completion notices by using a callback, you must implement a <a href="/windows/desktop/api/winbio/nc-winbio-pwinbio_async_completion_callback">PWINBIO_ASYNC_COMPLETION_CALLBACK</a> function and set the  <i>NotificationMethod</i> parameter to <b>WINBIO_ASYNC_NOTIFY_CALLBACK</b>.</li>
<li>If you choose to receive completion notices by using the application message queue, you must set the  <i>NotificationMethod</i> parameter to <b>WINBIO_ASYNC_NOTIFY_MESSAGE</b>. The framework returns a <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> pointer to the <b>LPARAM</b> field of the window message.</li>
</ul>
To prevent memory leaks, you must call <a href="/windows/desktop/api/winbio/nf-winbio-winbiofree">WinBioFree</a> to release the <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> structure after you have finished using it.

## -see-also

<a href="/windows/desktop/api/winbio/nf-winbio-winbiocontrolunitprivileged">WinBioControlUnitPrivileged</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbiolockunit">WinBioLockUnit</a>