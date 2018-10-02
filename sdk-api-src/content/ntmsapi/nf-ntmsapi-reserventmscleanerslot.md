---
UID: NF:ntmsapi.ReserveNtmsCleanerSlot
title: ReserveNtmsCleanerSlot function
author: windows-sdk-content
description: The ReserveNtmsCleanerSlot function reserves a single slot in a library unit for a drive cleaner cartridge.
old-location: fs\reserventmscleanerslot.htm
tech.root: Rsm
ms.assetid: 17e5acf8-c6b3-42a8-a9fe-fdda53779b67
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ReserveNtmsCleanerSlot, ReserveNtmsCleanerSlot function [Files], _zaw_reserventmscleanerslot, base.reserventmscleanerslot, fs.reserventmscleanerslot, ntmsapi/ReserveNtmsCleanerSlot
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntmsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntmsapi.lib
req.dll: Ntmsapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntmsapi.dll
api_name:
 - ReserveNtmsCleanerSlot
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ReserveNtmsCleanerSlot function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>ReserveNtmsCleanerSlot</b> function reserves a single slot in a library unit for a drive cleaner cartridge.


## -parameters




### -param hSession [in]

Handle to the session returned by the 
<a href="https://msdn.microsoft.com/5a323911-e99c-4f81-9580-0feac2f0a54e">OpenNtmsSession</a> function.


### -param lpLibrary [in]

Unique identifier of the library to reserve the cleaner slot.


### -param lpSlot [in]

Unique identifier of the slot that is to be reserved for a cleaner cartridge.


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
<dt><b>ERROR_ALREADY_RESERVED</b></dt>
</dl>
</td>
<td width="60%">
Either this slot or another slot in the library has already been reserved for cleaning. To change the cleaner cartridge slot, the currently reserved cleaner slot must be released first, using the 
<a href="https://msdn.microsoft.com/c3530534-c502-4168-8039-b5ce4f0a5816">ReleaseNtmsCleanerSlot</a> function.

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
The value that is specified in the <i>hSession</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_SLOT</b></dt>
</dl>
</td>
<td width="60%">
Unable to retrieve the slot definition from the database.

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
<dt><b>ERROR_SLOT_FULL</b></dt>
</dl>
</td>
<td width="60%">
A cleaner slot is not reserved. The slot specified has media in it. Reservation can only be performed on an empty slot.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SLOT_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
A cleaner slot is not reserved. The slot specified is currently not installed in the library. This error occurs if at least one cartridge magazine is missing from the library.

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



The slot reserved with the 
<b>ReserveNtmsCleanerSlot</b> function must be present and empty. The library must not already have a slot reserved for a cleaner cartridge.




## -see-also




<a href="https://msdn.microsoft.com/55a8e7c0-85fd-40c5-b5b9-46ad321761c4">CleanNtmsDrive</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb540727(v=VS.85).aspx">Cleaner Management Functions</a>



<a href="https://msdn.microsoft.com/a55a8f17-1a14-4267-ae39-1585e1090f21">EjectNtmsCleaner</a>



<a href="https://msdn.microsoft.com/973441cb-2ec4-4a8d-8e75-3c6d01552a59">InjectNtmsCleaner</a>



<a href="https://msdn.microsoft.com/c3530534-c502-4168-8039-b5ce4f0a5816">ReleaseNtmsCleanerSlot</a>
 

 

