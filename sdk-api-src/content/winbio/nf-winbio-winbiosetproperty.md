---
UID: NF:winbio.WinBioSetProperty
title: WinBioSetProperty function
author: windows-driver-content
description: Sets the value of a standard property associated with a biometric session, unit, template, or account. Starting with Windows 10, build 1607, this function is available to use with a mobile image.
old-location: secbiomet\winbiosetproperty.htm
old-project: SecBioMet
ms.assetid: 569AAEF0-DA06-4005-9874-2762BE96539F
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: WinBioSetProperty, WinBioSetProperty function [Windows Biometric Framework API], secbiomet.winbiosetproperty, winbio/WinBioSetProperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: WINBIO_ASYNC_NOTIFICATION_METHOD, *PWINBIO_ASYNC_NOTIFICATION_METHOD
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	winbio.dll
-	Ext-MS-Win-Biometrics-WinBio-Core-L1-1-0.dll
-	Ext-MS-Win-BioMetrics-WinBio-Core-L1-1-1.dll
api_name:
-	WinBioSetProperty
product: Windows
targetos: Windows
req.lib: Winbio.lib
req.dll: Winbio.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WinBioSetProperty function


## -description


Sets the value of   a standard property associated with a biometric session, unit, template, or account. Starting with Windows 10, build 1607, this  function is available to use with a mobile image.


## -parameters




### -param SessionHandle [in]

A <b>WINBIO_SESSION_HANDLE</b> value that identifies an open biometric session.  Open a synchronous session handle by calling <a href="https://msdn.microsoft.com/e9a0bb5f-4bbd-4dc4-9cd8-c26f5e4f74cf">WinBioOpenSession</a>. Open an asynchronous session handle by calling <a href="https://msdn.microsoft.com/711EDE14-A2EE-415D-8FB6-562D71D68146">WinBioAsyncOpenSession</a>.


### -param PropertyType [in]

A <b>WINBIO_PROPERTY_TYPE</b> value that specifies the type of the property that you want to set. Currently this must be <b>WINBIO_PROPERTY_TYPE_ACCOUNT</b>.


### -param PropertyId [in]

A <b>WINBIO_PROPERTY_ID</b> value that specifies the property to set. Currently this must be <b>WINBIO_PROPERTY_ANTI_SPOOF_POLICY</b>. All other properties are read-only.


### -param UnitId [in, optional]

A <b>WINBIO_UNIT_ID</b> value that identifies the biometric unit. For the <b>WINBIO_PROPERTY_ANTI_SPOOF_POLICY</b> property, this value must be 0.


### -param Identity [in, optional]

Address of a <a href="https://msdn.microsoft.com/58a5f4ba-2f58-466c-90fd-9480c3c095db">WINBIO_IDENTITY</a> structure that specifies the account for which you want to set the property.


### -param SubFactor [in, optional]

Reserved. This must be <b>WINBIO_SUBTYPE_NO_INFORMATION</b>.


### -param PropertyBuffer [in]

A pointer to a structure that specifies the new value for the property. This value cannot be NULL. For setting the <b>WINBIO_PROPERTY_ANTI_SPOOF_POLICY</b> property, the structure must be a <a href="https://msdn.microsoft.com/2B433AE8-21A0-4AF1-853C-9074527DB2E4">WINBIO_ANTI_SPOOF_POLICY</a> structure.


### -param PropertyBufferSize [in]

The size, in bytes, of the structure to which the <i>PropertyBuffer</i> parameter points. This value cannot be 0.


## -returns



If the function succeeds, it returns <b>S_OK</b>. If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

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



To use <b>WinBioSetProperty</b> synchronously, call the function with a session handle created by calling <a href="https://msdn.microsoft.com/e9a0bb5f-4bbd-4dc4-9cd8-c26f5e4f74cf">WinBioOpenSession</a>. The function blocks until the operation completes or an error is encountered. To prevent memory leaks, you must call <a href="https://msdn.microsoft.com/b570fc6c-a08e-4485-a621-20f59bd63d40">WinBioFree</a> to release the memory pointed to by the <i>PropertyBuffer</i> parameter when you are finished using the data contained in the buffer.

To use <b>WinBioSetProperty</b> asynchronously, call the function with a session handle created by calling <a href="https://msdn.microsoft.com/711EDE14-A2EE-415D-8FB6-562D71D68146">WinBioAsyncOpenSession</a>. The framework allocates a <a href="https://msdn.microsoft.com/1C8A4557-3851-4AB2-BB9B-AE199EB9D024">WINBIO_ASYNC_RESULT</a> structure  and uses it to return information about operation success or failure.  The <b>WINBIO_ASYNC_RESULT</b> structure is returned to the application callback or to the application message queue, depending on the value you set in the <i>NotificationMethod</i> parameter of the <b>WinBioAsyncOpenSession</b> function:

<ul>
<li>If you choose to receive completion notices by using a callback, you must implement a <a href="https://msdn.microsoft.com/550EA13D-18CE-4B73-9C9B-4D5C46C48A75">PWINBIO_ASYNC_COMPLETION_CALLBACK</a> function and set the  <i>NotificationMethod</i> parameter to <b>WINBIO_ASYNC_NOTIFY_CALLBACK</b>.</li>
<li>If you choose to receive completion notices by using the application message queue, you must set the  <i>NotificationMethod</i> parameter to <b>WINBIO_ASYNC_NOTIFY_MESSAGE</b>. The framework returns a <a href="https://msdn.microsoft.com/1C8A4557-3851-4AB2-BB9B-AE199EB9D024">WINBIO_ASYNC_RESULT</a> pointer to the <b>LPARAM</b> field of the window message.</li>
</ul>
To prevent memory leaks, you must call <a href="https://msdn.microsoft.com/b570fc6c-a08e-4485-a621-20f59bd63d40">WinBioFree</a> to release the <a href="https://msdn.microsoft.com/1C8A4557-3851-4AB2-BB9B-AE199EB9D024">WINBIO_ASYNC_RESULT</a> structure after you have finished using it.




## -see-also




<a href="https://msdn.microsoft.com/b570fc6c-a08e-4485-a621-20f59bd63d40">WinBioFree</a>



<a href="https://msdn.microsoft.com/63e38e74-3d46-4474-a31c-eaf724156bc6">WinBioGetProperty</a>
 

 

