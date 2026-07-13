---
UID: NF:winbio.WinBioSetProperty
title: WinBioSetProperty function (winbio.h)
description: Sets the value of a standard property associated with a biometric session, unit, template, or account. Starting with Windows 10, build 1607, this function is available to use with a mobile image.
helpviewer_keywords: ["WinBioSetProperty","WinBioSetProperty function [Windows Biometric Framework API]","secbiomet.winbiosetproperty","winbio/WinBioSetProperty"]
old-location: secbiomet\winbiosetproperty.htm
tech.root: SecBioMet
ms.assetid: 569AAEF0-DA06-4005-9874-2762BE96539F
ms.date: 12/05/2018
ms.keywords: WinBioSetProperty, WinBioSetProperty function [Windows Biometric Framework API], secbiomet.winbiosetproperty, winbio/WinBioSetProperty
req.header: winbio.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - WinBioSetProperty
 - winbio/WinBioSetProperty
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
 - winbio.dll
 - Ext-MS-Win-Biometrics-WinBio-Core-L1-1-0.dll
 - Ext-MS-Win-BioMetrics-WinBio-Core-L1-1-1.dll
api_name:
 - WinBioSetProperty
---

# WinBioSetProperty function


## -description

Sets the value of   a standard property associated with a biometric session, unit, template, or account. Starting with Windows 10, build 1607, this  function is available to use with a mobile image.

## -parameters

### -param SessionHandle [in]

A <b>WINBIO_SESSION_HANDLE</b> value that identifies an open biometric session.  Open a synchronous session handle by calling <a href="/windows/desktop/api/winbio/nf-winbio-winbioopensession">WinBioOpenSession</a>. Open an asynchronous session handle by calling <a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopensession">WinBioAsyncOpenSession</a>.

### -param PropertyType [in]

A <b>WINBIO_PROPERTY_TYPE</b> value that specifies the type of the property that you want to set. Currently this must be <b>WINBIO_PROPERTY_TYPE_ACCOUNT</b>.

### -param PropertyId [in]

A <b>WINBIO_PROPERTY_ID</b> value that specifies the property to set. Currently this must be <b>WINBIO_PROPERTY_ANTI_SPOOF_POLICY</b>. All other properties are read-only.

### -param UnitId [in, optional]

A <b>WINBIO_UNIT_ID</b> value that identifies the biometric unit. For the <b>WINBIO_PROPERTY_ANTI_SPOOF_POLICY</b> property, this value must be 0.

### -param Identity [in, optional]

Address of a <a href="/windows/desktop/SecBioMet/winbio-identity">WINBIO_IDENTITY</a> structure that specifies the account for which you want to set the property.

### -param SubFactor [in, optional]

Reserved. This must be <b>WINBIO_SUBTYPE_NO_INFORMATION</b>.

### -param PropertyBuffer [in]

A pointer to a structure that specifies the new value for the property. This value cannot be NULL. For setting the <b>WINBIO_PROPERTY_ANTI_SPOOF_POLICY</b> property, the structure must be a <a href="/windows/desktop/SecBioMet/winbio-anti-spoof-policy">WINBIO_ANTI_SPOOF_POLICY</a> structure.

### -param PropertyBufferSize [in]

The size, in bytes, of the structure to which the <i>PropertyBuffer</i> parameter points. This value cannot be 0.

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
The <i>Identity</i> and <i>PropertyBuffer</i> parameters cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>PropertyType</i>, <i>PropertyId</i>, or <i>PropertyBufferSize</i> parameter cannot be 0.

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
The caller attempted to set a property that resides inside of a locked region.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_UNSUPPORTED_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
The object does not support the specified property.

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

To use <b>WinBioSetProperty</b> synchronously, call the function with a session handle created by calling <a href="/windows/desktop/api/winbio/nf-winbio-winbioopensession">WinBioOpenSession</a>. The function blocks until the operation completes or an error is encountered. To prevent memory leaks, you must call <a href="/windows/desktop/api/winbio/nf-winbio-winbiofree">WinBioFree</a> to release the memory pointed to by the <i>PropertyBuffer</i> parameter when you are finished using the data contained in the buffer.

To use <b>WinBioSetProperty</b> asynchronously, call the function with a session handle created by calling <a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopensession">WinBioAsyncOpenSession</a>. The framework allocates a <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> structure  and uses it to return information about operation success or failure.  The <b>WINBIO_ASYNC_RESULT</b> structure is returned to the application callback or to the application message queue, depending on the value you set in the <i>NotificationMethod</i> parameter of the <b>WinBioAsyncOpenSession</b> function:

<ul>
<li>If you choose to receive completion notices by using a callback, you must implement a <a href="/windows/desktop/api/winbio/nc-winbio-pwinbio_async_completion_callback">PWINBIO_ASYNC_COMPLETION_CALLBACK</a> function and set the  <i>NotificationMethod</i> parameter to <b>WINBIO_ASYNC_NOTIFY_CALLBACK</b>.</li>
<li>If you choose to receive completion notices by using the application message queue, you must set the  <i>NotificationMethod</i> parameter to <b>WINBIO_ASYNC_NOTIFY_MESSAGE</b>. The framework returns a <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> pointer to the <b>LPARAM</b> field of the window message.</li>
</ul>
To prevent memory leaks, you must call <a href="/windows/desktop/api/winbio/nf-winbio-winbiofree">WinBioFree</a> to release the <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> structure after you have finished using it.

## -see-also

<a href="/windows/desktop/api/winbio/nf-winbio-winbiofree">WinBioFree</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbiogetproperty">WinBioGetProperty</a>