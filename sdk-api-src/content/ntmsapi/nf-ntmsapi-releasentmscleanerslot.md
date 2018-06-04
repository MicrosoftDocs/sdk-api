---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ReleaseNtmsCleanerSlot function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>ReleaseNtmsCleanerSlot</b> function removes an existing slot reservation for a cleaning cartridge. The slot can then be used for data cartridges.


## -parameters




### -param hSession [in]

Handle to the session returned by the 
<a href="https://msdn.microsoft.com/5a323911-e99c-4f81-9580-0feac2f0a54e">OpenNtmsSession</a> function.


### -param lpLibrary [in]

Unique identifier of the library to release the cleaner slot.


## -returns



This function returns one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
NTMS_CONTROL_ACCESS to the library is denied. Other security errors are also possible, but they would indicate a security subsystem error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DEVICE_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The library is not currently connected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The value specified in the <i>hSession</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
Unable to connect to the RSM service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SLOT_RESERVED</b></dt>
</dl>
</td>
<td width="60%">
This library has no slot reserved for a cleaner cartridge.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SLOT_FULL</b></dt>
</dl>
</td>
<td width="60%">
The library has a reserved cleaner cartridge slot but the slot contains a cleaner cartridge (the slot must be empty). Use the 
<a href="https://msdn.microsoft.com/a55a8f17-1a14-4267-ae39-1585e1090f21">EjectNtmsCleaner</a> function to eject a cleaner cartridge.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SLOT_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The library has a reserved cleaner cartridge slot, but the specified slot is currently not installed in the library. This error can occur if at least one magazine is missing from the library.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was queued successfully.

</td>
</tr>
</table>
 




## -remarks



For the 
<b>ReleaseNtmsCleanerSlot</b> function to succeed, the slot must be present and empty. The library must also have a slot reserved for cleaning.




## -see-also




<a href="https://msdn.microsoft.com/55a8e7c0-85fd-40c5-b5b9-46ad321761c4">CleanNtmsDrive</a>



<a href="removable_storage_manager_functions.htm">Cleaner Management Functions</a>



<a href="https://msdn.microsoft.com/a55a8f17-1a14-4267-ae39-1585e1090f21">EjectNtmsCleaner</a>



<a href="https://msdn.microsoft.com/973441cb-2ec4-4a8d-8e75-3c6d01552a59">InjectNtmsCleaner</a>



<a href="https://msdn.microsoft.com/17e5acf8-c6b3-42a8-a9fe-fdda53779b67">ReserveNtmsCleanerSlot</a>
 

 

