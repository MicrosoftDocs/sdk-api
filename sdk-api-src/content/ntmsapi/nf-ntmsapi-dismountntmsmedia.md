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

# DismountNtmsMedia function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>DismountNtmsMedia</b> function queues a command to move the specified media in a drive to its storage. This function should be paired with the 
<a href="https://msdn.microsoft.com/f943f36c-654a-48ed-aeb2-1fc146f2d9ff">MountNtmsMedia</a> function.


## -parameters




### -param hSession [in]

Handle to the session returned by the 
<a href="https://msdn.microsoft.com/5a323911-e99c-4f81-9580-0feac2f0a54e">OpenNtmsSession</a> function.


### -param lpMediaId [in]

Array of at least one logical medium or side.


### -param dwCount [in]

Number of media identifiers in the <i>lpMediaId</i> parameter.


### -param dwOptions [in]

Options. This parameter can be the following value. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_DISMOUNT_DEFERRED"></a><a id="ntms_dismount_deferred"></a><dl>
<dt><b>NTMS_DISMOUNT_DEFERRED</b></dt>
</dl>
</td>
<td width="60%">
Marks media state as Dismountable, and keeps the medium in the drive. Subsequent mount requests are satisfied using dismounted or dismountable drives. The default is to dismount immediately.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_DISMOUNT_IMMEDIATE"></a><a id="ntms_dismount_immediate"></a><dl>
<dt><b>NTMS_DISMOUNT_IMMEDIATE</b></dt>
</dl>
</td>
<td width="60%">
Dismount the drive immediately.

</td>
</tr>
</table>
 


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
NTMS_USE_ACCESS to the media pool or library that contains the media is denied. Other security errors are also possible, but they would indicate a security subsystem error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DATABASE_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The database is inaccessible or damaged.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DATABASE_FULL</b></dt>
</dl>
</td>
<td width="60%">
The database is full.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DEVICE_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
One or more resources required to perform the dismount are not currently available (probably disabled).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_LIBRARY</b></dt>
</dl>
</td>
<td width="60%">
The library that contains the media is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_MEDIA</b></dt>
</dl>
</td>
<td width="60%">
At least one of the specified media is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
An unexpected media or device state occurred during dismount.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MEDIA_OFFLINE</b></dt>
</dl>
</td>
<td width="60%">
The specified media is offline.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MEDIA_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
One or more media resources required to perform the mount are not currently available (probably disabled).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred during processing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The media dismount has been queued.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The time-out event expired while the application attempted to acquire one or more resources.

</td>
</tr>
</table>
 




## -remarks



An application must use the 
<b>DismountNtmsMedia</b> function to release the drive resource after the application has used the specified medium. Unreleased media cannot be used by other RSM sessions.

The 
<b>DismountNtmsMedia</b> function returns as soon as the operation is queued with RSM. The application can wait for the side state to become idle.




## -see-also




<a href="removable_storage_manager_functions.htm">Media Services Functions</a>



<a href="https://msdn.microsoft.com/f943f36c-654a-48ed-aeb2-1fc146f2d9ff">MountNtmsMedia</a>
 

 

