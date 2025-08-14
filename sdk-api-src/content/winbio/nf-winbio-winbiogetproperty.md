---
UID: NF:winbio.WinBioGetProperty
title: WinBioGetProperty function (winbio.h)
description: Retrieves a session, unit, or template property. Starting with Windows 10, build 1607, this function is available to use with a mobile image.
helpviewer_keywords: ["WINBIO_PROPERTY_ANTI_SPOOF_POLICY","WINBIO_PROPERTY_EXTENDED_ENGINE_INFO","WINBIO_PROPERTY_EXTENDED_ENROLLMENT_STATUS","WINBIO_PROPERTY_EXTENDED_SENSOR_INFO","WINBIO_PROPERTY_EXTENDED_STORAGE_INFO","WINBIO_PROPERTY_SAMPLE_HINT","WinBioGetProperty","WinBioGetProperty function [Windows Biometric Framework API]","secbiomet.winbiogetproperty","winbio/WinBioGetProperty"]
old-location: secbiomet\winbiogetproperty.htm
tech.root: SecBioMet
ms.assetid: 63e38e74-3d46-4474-a31c-eaf724156bc6
ms.date: 12/05/2018
ms.keywords: WINBIO_PROPERTY_ANTI_SPOOF_POLICY, WINBIO_PROPERTY_EXTENDED_ENGINE_INFO, WINBIO_PROPERTY_EXTENDED_ENROLLMENT_STATUS, WINBIO_PROPERTY_EXTENDED_SENSOR_INFO, WINBIO_PROPERTY_EXTENDED_STORAGE_INFO, WINBIO_PROPERTY_SAMPLE_HINT, WinBioGetProperty, WinBioGetProperty function [Windows Biometric Framework API], secbiomet.winbiogetproperty, winbio/WinBioGetProperty
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
 - WinBioGetProperty
 - winbio/WinBioGetProperty
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
 - ext-ms-win-biometrics-winbio-core-l1-1-0.dll
 - Ext-MS-Win-BioMetrics-WinBio-Core-L1-1-1.dll
api_name:
 - WinBioGetProperty
---

# WinBioGetProperty function


## -description

Retrieves  a session, unit, or template property. Starting with Windows 10, build 1607, this  function is available to use with a mobile image.

## -parameters

### -param SessionHandle [in]

A <b>WINBIO_SESSION_HANDLE</b> value that identifies an open biometric session.  Open a synchronous session handle by calling <a href="/windows/desktop/api/winbio/nf-winbio-winbioopensession">WinBioOpenSession</a>. Open an asynchronous session handle by calling <a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopensession">WinBioAsyncOpenSession</a>.

### -param PropertyType [in]

A <b>WINBIO_PROPERTY_TYPE</b> value that specifies the source of the property information. Currently this must be <b>WINBIO_PROPERTY_TYPE_UNIT</b> or <b>WINBIO_PROPERTY_TYPE_ACCOUNT</b>. For more information about property types, see <a href="/windows/desktop/SecBioMet/winbio-property-type-constants">WINBIO_PROPERTY_TYPE Constants</a>.

The <b>WINBIO_PROPERTY_TYPE_ACCOUNT</b> value is supported starting in Windows 10.

### -param PropertyId [in]

A <b>WINBIO_PROPERTY_ID</b> value that specifies the property that you want to query. The following values are possible.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINBIO_PROPERTY_SAMPLE_HINT"></a><a id="winbio_property_sample_hint"></a><dl>
<dt><b><b>WINBIO_PROPERTY_SAMPLE_HINT</b></b></dt>
</dl>
</td>
<td width="60%">
Estimates the maximum number of good biometric samples that are required to complete an enrollment template. The result of the property query is returned in the buffer to which to the <i>PropertyBuffer</i> parameter points as a <b>ULONG</b> value that contains the hint.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_PROPERTY_EXTENDED_SENSOR_INFO_"></a><a id="winbio_property_extended_sensor_info_"></a><dl>
<dt><b><b>WINBIO_PROPERTY_EXTENDED_SENSOR_INFO </b></b></dt>
</dl>
</td>
<td width="60%">
Contains extended information about the capabilities and attributes of the sensor component that is connected to a specific biometric unit. The result of the property query is returned in the buffer to which to the <i>PropertyBuffer</i> parameter points as a <a href="/windows/desktop/SecBioMet/winbio-extended-sensor-info">WINBIO_EXTENDED_SENSOR_INFO</a> structure.
 This value is supported starting in Windows 10.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_PROPERTY_EXTENDED_ENGINE_INFO__"></a><a id="winbio_property_extended_engine_info__"></a><dl>
<dt><b><b>WINBIO_PROPERTY_EXTENDED_ENGINE_INFO  </b></b></dt>
</dl>
</td>
<td width="60%">
Contains extended information about the capabilities and attributes of the engine component that is connected to a specific biometric unit. The result of the property query is returned in the buffer to which to the <i>PropertyBuffer</i> parameter points as a <a href="/windows/desktop/SecBioMet/winbio-extended-engine-info">WINBIO_EXTENDED_ENGINE_INFO</a> structure.
This value is supported starting in Windows 10.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_PROPERTY_EXTENDED_STORAGE_INFO_"></a><a id="winbio_property_extended_storage_info_"></a><dl>
<dt><b><b>WINBIO_PROPERTY_EXTENDED_STORAGE_INFO </b></b></dt>
</dl>
</td>
<td width="60%">
Contains extended information about the capabilities and attributes of the storage component that is connected to a specific biometric unit. The result of the property query is returned in the buffer to which to the <i>PropertyBuffer</i> parameter points as a <a href="/windows/desktop/SecBioMet/winbio-extended-storage-info">WINBIO_EXTENDED_STORAGE_INFO</a> structure.
This value is supported starting in Windows 10.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_PROPERTY_EXTENDED_ENROLLMENT_STATUS_"></a><a id="winbio_property_extended_enrollment_status_"></a><dl>
<dt><b><b>WINBIO_PROPERTY_EXTENDED_ENROLLMENT_STATUS </b></b></dt>
</dl>
</td>
<td width="60%">
Contains extended information about the status of an enrollment that is in progress on a specific biometric unit. The result of the property query is returned in the buffer to which to the <i>PropertyBuffer</i> parameter points as a <a href="/windows/desktop/SecBioMet/winbio-extended-enrollment-status">WINBIO_EXTENDED_ENROLLMENT_STATUS</a> structure. If no enrollment is in progress on the biometric unit, the <b>TemplateStatus</b> member of the returned structure has a value of <b>WINBIO_E_INVALID_OPERATION</b>.
This value is supported starting in Windows 10.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_PROPERTY_ANTI_SPOOF_POLICY___"></a><a id="winbio_property_anti_spoof_policy___"></a><dl>
<dt><b><b>WINBIO_PROPERTY_ANTI_SPOOF_POLICY   </b></b></dt>
</dl>
</td>
<td width="60%">
Contains the values of the antispoofing policy for a specific user account. The property operation is returned in the buffer to which to the <i>PropertyBuffer</i> parameter points as a <a href="/windows/desktop/SecBioMet/winbio-anti-spoof-policy">WINBIO_ANTI_SPOOF_POLICY</a> structure.
This value is supported starting in Windows 10.

</td>
</tr>
</table>
 

For more information about these properties, see <a href="/windows/desktop/SecBioMet/winbio-property-constants">WINBIO_PROPERTY Constants</a>.

### -param UnitId [in, optional]

A <b>WINBIO_UNIT_ID</b> value that identifies the biometric unit. You can find a  unit identifier by calling the <a href="/windows/desktop/api/winbio/nf-winbio-winbioenumbiometricunits">WinBioEnumBiometricUnits</a> or <a href="/windows/desktop/api/winbio/nf-winbio-winbiolocatesensor">WinBioLocateSensor</a> functions.

If you specify <b>WINBIO_PROPERTY_ANTI_SPOOF_POLICY</b> as the value for the <i>PropertyId</i> parameter, specify 0 for the <i>UnitId</i> parameter. If you specify any other property with the <i>PropertyId</i> parameter, you cannot specify 0 for the <i>UnitId</i> parameter.

### -param Identity [in, optional]

A <a href="/windows/desktop/SecBioMet/winbio-identity">WINBIO_IDENTITY</a> structure that provides the SID of the account for which you want to get the antispoofing policy, if you specify <b>WINBIO_PROPERTY_ANTI_SPOOF_POLICY</b> as the value of the  <i>PropertyId</i> parameter.

If you specify any other value for the <i>PropertyId</i> parameter,  the <i>Identity</i> parameter  must be <b>NULL</b>.

### -param SubFactor [in, optional]

Reserved. This must be <b>WINBIO_SUBTYPE_NO_INFORMATION</b>.

### -param PropertyBuffer

Address of a pointer to a buffer that receives the property value. For information about the contents of this buffer for different properties, see the descriptions of the property values for the <i>PropertyId</i> parameter.

### -param PropertyBufferSize [out, optional]

Pointer to a variable that receives the size, in bytes, of the buffer pointed to by the <i>PropertyBuffer</i> parameter.

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
The session handle specified by the <i>SessionHandle</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>Identity</i>, <i>PropertyBuffer</i>, or <i>PropertyBufferSize</i> arguments cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>UnitId</i>, <i>Identity</i>, or <i>SubFactor</i> arguments are incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_INVALID_PROPERTY_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The value of the <i>PropertyType</i> argument is incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_INVALID_PROPERTY_ID</b></dt>
</dl>
</td>
<td width="60%">
The value of the <i>PropertyId</i> argument is incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_LOCK_VIOLATION</b></dt>
</dl>
</td>
<td width="60%">
The caller attempted to query a property that resides inside of a locked region.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_UNSUPPORTED_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
The object being queried does not support the specified property.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_ENROLLMENT_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
The operation could not be completed because the specified biometric unit is currently being used for an enrollment transaction (system pool only).

</td>
</tr>
</table>

## -remarks

To use <b>WinBioGetProperty</b> synchronously, call the function with a session handle created by calling <a href="/windows/desktop/api/winbio/nf-winbio-winbioopensession">WinBioOpenSession</a>. The function blocks until the operation completes or an error is encountered. To prevent memory leaks when you use <b>WinBioGetProperty</b> synchronously, you must call <a href="/windows/desktop/api/winbio/nf-winbio-winbiofree">WinBioFree</a> to release the memory pointed to by the <i>PropertyBuffer</i> parameter when you are finished using the data contained in the buffer.

To use <b>WinBioGetProperty</b> asynchronously, call the function with a session handle created by calling <a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopensession">WinBioAsyncOpenSession</a>. The framework allocates a <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> structure  and uses it to return information about operation success or failure. If the operation is successful, the framework returns information in a nested <b>GetProperty</b> structure. The <b>WINBIO_ASYNC_RESULT</b> structure is returned to the application callback or to the application message queue, depending on the value you set in the <i>NotificationMethod</i> parameter of the <b>WinBioAsyncOpenSession</b> function:

<ul>
<li>If you choose to receive completion notices by using a callback, you must implement a <a href="/windows/desktop/api/winbio/nc-winbio-pwinbio_async_completion_callback">PWINBIO_ASYNC_COMPLETION_CALLBACK</a> function and set the  <i>NotificationMethod</i> parameter to <b>WINBIO_ASYNC_NOTIFY_CALLBACK</b>.</li>
<li>If you choose to receive completion notices by using the application message queue, you must set the  <i>NotificationMethod</i> parameter to <b>WINBIO_ASYNC_NOTIFY_MESSAGE</b>. The framework returns a <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> pointer to the <b>LPARAM</b> field of the window message.</li>
</ul>
To prevent memory leaks when you use <b>WinBioGetProperty</b> asynchronously, you must call <a href="/windows/desktop/api/winbio/nf-winbio-winbiofree">WinBioFree</a> to release the <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> structure after you have finished using it. The <b>WINBIO_ASYNC_RESULT</b> structure and the property buffer occupy a single block of memory, so your application only needs to pass the address of the <b>WINBIO_ASYNC_RESULT</b> structure to <b>WinBioFree</b>. When you call <b>WinBioFree</b> this way, <b>WinBioFree</b> automatically releases both the <b>WINBIO_ASYNC_RESULT</b> structure and the property buffer. If you try to release the property buffer separately in this case, the application stops responding.

## -see-also

<a href="/windows/desktop/api/winbio/nf-winbio-winbiofree">WinBioFree</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbiosetproperty">WinBioSetProperty</a>