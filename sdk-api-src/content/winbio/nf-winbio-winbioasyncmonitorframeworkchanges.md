---
UID: NF:winbio.WinBioAsyncMonitorFrameworkChanges
title: WinBioAsyncMonitorFrameworkChanges function
author: windows-sdk-content
description: Starts an asynchronous monitor of changes to the biometric framework.
old-location: secbiomet\winbioasyncmonitorframeworkchanges.htm
tech.root: SecBioMet
ms.assetid: 4BA91B17-DA7D-456C-A815-ED25A3C5D74A
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WINBIO_FRAMEWORK_CHANGE_UNIT, WinBioAsyncMonitorFrameworkChanges, WinBioAsyncMonitorFrameworkChanges function [Windows Biometric Framework API], secbiomet.winbioasyncmonitorframeworkchanges, winbio/WinBioAsyncMonitorFrameworkChanges
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - WinBioExt.dll
 - Ext-MS-Win-BioMetrics-WinBio-l1-2-0.dll
 - Ext-MS-Win-BioMetrics-WinBio-L1-3-0.dll
api_name:
 - WinBioAsyncMonitorFrameworkChanges
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- WinBioAsyncMonitorFrameworkChanges
: 
---

# WinBioAsyncMonitorFrameworkChanges function


## -description


Starts an asynchronous monitor of changes to the biometric framework. Currently, the only monitored changes that are supported occur when a biometric unit is attached to or detached from the computer.


## -parameters




### -param FrameworkHandle [in]

Handle to the framework session opened by calling <a href="https://msdn.microsoft.com/D9557A6F-32C4-464F-8800-6E546808F100">WinBioAsyncOpenFramework</a>.


### -param ChangeTypes [in]

A bitmask of type <b>WINBIO_FRAMEWORK_CHANGE_TYPE</b> flags that indicates the types of events that should generate asynchronous notifications. Beginning with  Windows 8, the following flag is available:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINBIO_FRAMEWORK_CHANGE_UNIT"></a><a id="winbio_framework_change_unit"></a><dl>
<dt><b>WINBIO_FRAMEWORK_CHANGE_UNIT</b></dt>
</dl>
</td>
<td width="60%">
A biometric unit has been attached to or detached from the computer.

</td>
</tr>
</table>
 


## -returns



The function returns an <b>HRESULT</b> indicating success or failure. Note that success indicates only that the function arguments were valid. Failures encountered during the execution of the operation will be returned asynchronously to a <a href="https://msdn.microsoft.com/1C8A4557-3851-4AB2-BB9B-AE199EB9D024">WINBIO_ASYNC_RESULT</a> structure using the notification method specified in <a href="https://msdn.microsoft.com/D9557A6F-32C4-464F-8800-6E546808F100">WinBioAsyncOpenFramework</a>.

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
The bitmask contained in the <i>ChangeTypes</i> parameter contains one or more an invalid type bits. Currently, the only available value is <b>WINBIO_FRAMEWORK_CHANGE_UNIT</b>.

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
</table>
 




## -remarks



Once started, this monitor will continue generating events until the client application calls <a href="https://msdn.microsoft.com/62176608-1545-47d2-b4be-37bb2a4a064b">WinBioCancel</a> or <a href="https://msdn.microsoft.com/AE13FB2F-0B6B-4D98-A75A-E8A2EA525136">WinBioCloseFramework</a>. Creating a monitor for <b>WINBIO_FRAMEWORK_CHANGE_UNIT</b> events will generate two types of asynchronous notifications:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
<b>WINBIO_OPERATION_UNIT_ARRIVAL</b>

</td>
<td>
A biometric unit is attached.

</td>
</tr>
<tr>
<td>
<b>WINBIO_OPERATION_UNIT_REMOVAL</b>

</td>
<td>
A biometric unit is detached.

</td>
</tr>
</table>
 

The <b>WinBioAsyncMonitorFrameworkChanges</b> function uses a handle to the framework session opened by calling <a href="https://msdn.microsoft.com/D9557A6F-32C4-464F-8800-6E546808F100">WinBioAsyncOpenFramework</a>.  The framework allocates a <a href="https://msdn.microsoft.com/1C8A4557-3851-4AB2-BB9B-AE199EB9D024">WINBIO_ASYNC_RESULT</a> structure  and uses it to return information about operation success or failure. If a biometric unit is attached to or detached from the computer, the framework sets the <b>Operation</b> member of the structure. If a problem is encountered during the operation, the framework uses the <b>WINBIO_ASYNC_RESULT</b> structure to return error information. The structure is returned to the application callback or to the application message queue, depending on the value you set in the <i>NotificationMethod</i> parameter of the <b>WinBioAsyncOpenFramework</b> function.

<ul>
<li>If you choose to receive completion notices by using a callback, you must implement a <a href="https://msdn.microsoft.com/550EA13D-18CE-4B73-9C9B-4D5C46C48A75">PWINBIO_ASYNC_COMPLETION_CALLBACK</a> function and set the  <i>NotificationMethod</i> parameter to <b>WINBIO_ASYNC_NOTIFY_CALLBACK</b>.</li>
<li>If you choose to receive completion notices by using the application message queue, you must set the  <i>NotificationMethod</i> parameter to <b>WINBIO_ASYNC_NOTIFY_MESSAGE</b>. The framework returns a <a href="https://msdn.microsoft.com/1C8A4557-3851-4AB2-BB9B-AE199EB9D024">WINBIO_ASYNC_RESULT</a> pointer to the <b>LPARAM</b> field of the window message.</li>
</ul>
Notifications are   returned in an <b>EnumServiceProviders</b> structure nested inside the <a href="https://msdn.microsoft.com/1C8A4557-3851-4AB2-BB9B-AE199EB9D024">WINBIO_ASYNC_RESULT</a> structure. You must call <a href="https://msdn.microsoft.com/b570fc6c-a08e-4485-a621-20f59bd63d40">WinBioFree</a> to release the <b>WINBIO_ASYNC_RESULT</b> structure after you have finished using it.




## -see-also




<a href="https://msdn.microsoft.com/D9557A6F-32C4-464F-8800-6E546808F100">WinBioAsyncOpenFramework</a>
 

 

