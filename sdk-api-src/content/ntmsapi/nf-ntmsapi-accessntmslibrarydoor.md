---
UID: NF:ntmsapi.AccessNtmsLibraryDoor
title: AccessNtmsLibraryDoor function
author: windows-sdk-content
description: The AccessNtmsLibraryDoor function unlocks the door of the specified library. If the library is busy, RSM queues the request and returns successfully.
old-location: fs\accessntmslibrarydoor.htm
old-project: Rsm
ms.assetid: c7bc4582-4405-4e42-a8bf-e2e8c68bbd7e
ms.author: windowssdkdev
ms.date: 04/05/2018
ms.keywords: AccessNtmsLibraryDoor, AccessNtmsLibraryDoor function [Files], NTMS_INVENTORY_DEFAULT, NTMS_INVENTORY_FAST, NTMS_INVENTORY_NONE, NTMS_INVENTORY_OMID, _zaw_accessntmslibrarydoor, base.accessntmslibrarydoor, fs.accessntmslibrarydoor, ntmsapi/AccessNtmsLibraryDoor
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntmsapi.dll
api_name:
 - AccessNtmsLibraryDoor
product: Windows
targetos: Windows
req.lib: Ntmsapi.lib
req.dll: Ntmsapi.dll
req.irql: 
req.product: ADAM
---

# AccessNtmsLibraryDoor function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>AccessNtmsLibraryDoor</b> function unlocks the door of the specified library. If the library is busy, RSM queues the request and returns successfully.


## -parameters




### -param hSession [in]

Handle to the session returned by the 
<a href="https://msdn.microsoft.com/5a323911-e99c-4f81-9580-0feac2f0a54e">OpenNtmsSession</a> function.


### -param lpLibraryId [in]

Unique identifier of the library object. This library must support door access.


### -param dwAction [in]

Action to perform. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_INVENTORY_NONE"></a><a id="ntms_inventory_none"></a><dl>
<dt><b>NTMS_INVENTORY_NONE</b></dt>
</dl>
</td>
<td width="60%">
After the user closes the door, no inventory is performed. However, if a mount-label check fails, an inventory will be performed.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_INVENTORY_OMID"></a><a id="ntms_inventory_omid"></a><dl>
<dt><b>NTMS_INVENTORY_OMID</b></dt>
</dl>
</td>
<td width="60%">
After the user closes the door, a full on-media inventory is performed. This can be time consuming because each side of each medium must be mounted.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_INVENTORY_FAST"></a><a id="ntms_inventory_fast"></a><dl>
<dt><b>NTMS_INVENTORY_FAST</b></dt>
</dl>
</td>
<td width="60%">
If the library has a bar-code reader installed, this flag causes bar-code inventory to be performed. If the library does not have a bar-code reader, this flag causes a differential inventory to be performed. The OMIDs are checked on each medium placed in an empty slot while the door is open.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_INVENTORY_DEFAULT"></a><a id="ntms_inventory_default"></a><dl>
<dt><b>NTMS_INVENTORY_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
Use the <b>InventoryMethod</b> specified in the library object (see 
<a href="https://msdn.microsoft.com/f8ca33ba-35e2-4fd9-a9a0-1393bbbede80">NTMS_LIBRARYINFORMATION</a>).

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
NTMS_CONTROL_ACCESS to the library is denied. Other security errors are also possible, but they would indicate a security subsystem error.

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
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The session ID is missing or is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The library ID is missing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_LIBRARY_OFFLINE</b></dt>
</dl>
</td>
<td width="60%">
The library ID references an offline library without a door.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
An allocation failure occurred during processing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_RESOURCE_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
The library is disabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_RESOURCE_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The library does not have a door.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
Door access is queued.

</td>
</tr>
</table>
 




## -remarks



Some libraries provide no means for RSM to programmatically lock and unlock their doors. The behavior of this function with these libraries is identical to its behavior with libraries that RSM can unlock and lock.




## -see-also




<a href="https://msdn.microsoft.com/ecb7374c-d1fa-4e7c-87ad-045122cb466e">EjectNtmsMedia</a>



<a href="https://msdn.microsoft.com/c4274c9c-f052-42dd-859b-85606d455001">InjectNtmsMedia</a>



<a href="https://msdn.microsoft.com/library/Bb540727(v=VS.85).aspx">Library Control Functions</a>
 

 

