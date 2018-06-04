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

# InventoryNtmsLibrary function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>InventoryNtmsLibrary</b> function queues an inventory of the specified library. If the library is busy, RSM queues 
<b>InventoryNtmsLibrary</b> and returns success.


## -parameters




### -param hSession [in]

Handle to the session returned by the 
<a href="https://msdn.microsoft.com/5a323911-e99c-4f81-9580-0feac2f0a54e">OpenNtmsSession</a> function.


### -param lpLibraryId [in]

Unique identifier of a library object.


### -param dwAction [in]

Action to perform. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_INVENTORY_OMID"></a><a id="ntms_inventory_omid"></a><dl>
<dt><b>NTMS_INVENTORY_OMID</b></dt>
</dl>
</td>
<td width="60%">
A full on-media inventory is performed. Each side of each medium must be mounted into a drive. This is a time consuming process.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_INVENTORY_FAST"></a><a id="ntms_inventory_fast"></a><dl>
<dt><b>NTMS_INVENTORY_FAST</b></dt>
</dl>
</td>
<td width="60%">
If the library has a bar-code reader installed, this flag causes a bar-code inventory to be performed. If the library does not have a bar-code reader, this flag causes a differential inventory to be performed (slots are classified).

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
<tr>
<td width="40%"><a id="NTMS_INVENTORY_STOP"></a><a id="ntms_inventory_stop"></a><dl>
<dt><b>NTMS_INVENTORY_STOP</b></dt>
</dl>
</td>
<td width="60%">
Stop the current inventory in the specified library.

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
Access to one or more RSM objects is denied.

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
<dt><b>ERROR_INVALID_LIBRARY</b></dt>
</dl>
</td>
<td width="60%">
The library is the offline library.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The library ID or session ID is not valid.

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
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
</table>
 




## -remarks



Not present libraries cannot be inventoried.

The 
<b>InventoryNtmsLibrary</b> function marks all the slots that currently contain a medium in the library for classification/identification. The 
<b>InventoryNtmsLibrary</b> function returns when all the media is marked.




## -see-also




<a href="https://msdn.microsoft.com/c7bc4582-4405-4e42-a8bf-e2e8c68bbd7e">AccessNtmsLibraryDoor</a>



<a href="removable_storage_manager_functions.htm">Library Control Functions</a>
 

 

