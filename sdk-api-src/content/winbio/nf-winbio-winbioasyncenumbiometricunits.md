---
UID: NF:winbio.WinBioAsyncEnumBiometricUnits
title: WinBioAsyncEnumBiometricUnits function (winbio.h)
author: windows-sdk-content
description: Asynchronously enumerates all attached biometric units that match the input factor type.
old-location: secbiomet\winbioasyncenumbiometricunits.htm
tech.root: SecBioMet
ms.assetid: 3A7CEC71-7352-43B7-83D3-447D487C4703
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WinBioAsyncEnumBiometricUnits, WinBioAsyncEnumBiometricUnits function [Windows Biometric Framework API], secbiomet.winbioasyncenumbiometricunits, winbio/WinBioAsyncEnumBiometricUnits
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winbio.dll
 - Ext-MS-Win-BioMetrics-WinBio-Core-l1-1-0.dll
 - Ext-MS-Win-BioMetrics-WinBio-Core-L1-1-1.dll
api_name:
 - WinBioAsyncEnumBiometricUnits
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WinBioAsyncEnumBiometricUnits function


## -description


Asynchronously enumerates all attached biometric units that match the input factor type. For a synchronous version of this function, see <a href="https://msdn.microsoft.com/e1ca5712-978e-4e31-a941-eb462c670eac">WinBioEnumBiometricUnits</a>. Starting with Windows 10, build 1607, this  function is available to use with a mobile image.


## -parameters




### -param FrameworkHandle [in]

Handle to the framework session opened by calling  <a href="https://msdn.microsoft.com/D9557A6F-32C4-464F-8800-6E546808F100">WinBioAsyncOpenFramework</a>.


### -param Factor [in]

A bitmask of <a href="https://msdn.microsoft.com/7a15969c-ea64-464e-bd16-1daf0f2ea26f">WINBIO_BIOMETRIC_TYPE</a> flags that specifies the biometric unit types to be enumerated.  Only <b>WINBIO_TYPE_FINGERPRINT</b> is currently supported.


## -returns



The function returns an <b>HRESULT</b> indicating success or failure. Note that success indicates only that the arguments were valid. Failures encountered during the execution of the operation will be returned asynchronously to a <a href="https://msdn.microsoft.com/1C8A4557-3851-4AB2-BB9B-AE199EB9D024">WINBIO_ASYNC_RESULT</a> structure using the notification method specified in the call to <a href="https://msdn.microsoft.com/D9557A6F-32C4-464F-8800-6E546808F100">WinBioAsyncOpenFramework</a>.

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
You must set the <i>FrameworkHandle</i> argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The bitmask contained in the <i>Factor</i> parameter contains one or more an invalid type bits.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to complete the request.

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
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_INCORRECT_SESSION_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The <i>FrameworkHandle</i> argument must represent an asynchronous framework session.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_SESSION_HANDLE_CLOSED</b></dt>
</dl>
</td>
<td width="60%">
The session handle has been marked for closure.

</td>
</tr>
</table>
 




## -remarks



The <b>WinBioAsyncEnumBiometricUnits</b> function uses a handle to the framework session opened by calling <a href="https://msdn.microsoft.com/D9557A6F-32C4-464F-8800-6E546808F100">WinBioAsyncOpenFramework</a>.  The framework allocates a <a href="https://msdn.microsoft.com/1C8A4557-3851-4AB2-BB9B-AE199EB9D024">WINBIO_ASYNC_RESULT</a> structure  and uses it to return information about operation success or failure. If the enumeration operation is successful, the framework returns an array of schemas that include information about each enumerated biometric unit. If the operation is unsuccessful, the framework uses the <b>WINBIO_ASYNC_RESULT</b> structure to return error information. The structure is returned to the application callback or to the application message queue, depending on the value you set in the <i>NotificationMethod</i> parameter of the <b>WinBioAsyncOpenFramework</b> function.

<ul>
<li>If you choose to receive completion notices by using a callback, you must implement a <a href="https://msdn.microsoft.com/550EA13D-18CE-4B73-9C9B-4D5C46C48A75">PWINBIO_ASYNC_COMPLETION_CALLBACK</a> function and set the  <i>NotificationMethod</i> parameter to <b>WINBIO_ASYNC_NOTIFY_CALLBACK</b>.</li>
<li>If you choose to receive completion notices by using the application message queue, you must set the  <i>NotificationMethod</i> parameter to <b>WINBIO_ASYNC_NOTIFY_MESSAGE</b>. The framework returns a <a href="https://msdn.microsoft.com/1C8A4557-3851-4AB2-BB9B-AE199EB9D024">WINBIO_ASYNC_RESULT</a> pointer to the <b>LPARAM</b> field of the window message.</li>
</ul>
The  array of schemas is  returned in an <b>EnumBiometricUnits</b> structure nested inside the <a href="https://msdn.microsoft.com/1C8A4557-3851-4AB2-BB9B-AE199EB9D024">WINBIO_ASYNC_RESULT</a> structure. You must call <a href="https://msdn.microsoft.com/b570fc6c-a08e-4485-a621-20f59bd63d40">WinBioFree</a> to release the <b>WINBIO_ASYNC_RESULT</b> structure after you have finished using it.

Calling <b>WinBioAsyncEnumBiometricUnits</b> causes a single notification to be sent to the client application.




## -see-also




<a href="https://msdn.microsoft.com/D9557A6F-32C4-464F-8800-6E546808F100">WinBioAsyncOpenFramework</a>
 

 

