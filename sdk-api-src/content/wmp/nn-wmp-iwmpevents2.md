---
UID: NN:wmp.IWMPEvents2
title: IWMPEvents2
author: windows-sdk-content
description: The IWMPEvents2 interface provides events originating from the Windows Media Player 10 or later control to which an embedding program can respond. The events exposed by IWMPEvents2 are also exposed by the _WMPOCXEvents interface.
old-location: wmp\iwmpevents2_interface.htm
tech.root: WMP
ms.assetid: 61cd0a2e-b94f-4c10-b3e2-ad1dc2a0b17d
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IWMPEvents2, IWMPEvents2 interface [Windows Media Player], IWMPEvents2 interface [Windows Media Player],described, IWMPEvents2Interface, wmp.iwmpevents2_interface, wmp/IWMPEvents2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmp.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.h
api_name:
 - IWMPEvents2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPEvents2 interface


## -description



The <b>IWMPEvents2</b> interface provides events originating from the Windows Media Player 10 or later control to which an embedding program can respond. The events exposed by <b>IWMPEvents2</b> are also exposed by the <b>_WMPOCXEvents</b> interface.



The events provided by <b>IWMPEvents2</b> are related to device synchronization. To receive these events you must create a remoted instance of the Windows Media Player 10 or later control.

In addition to the methods inherited from <b>IWMPEvents</b>, the <b>IWMPEvents2</b> interface exposes the following methods.
<table>
<tr>
<th>Method
          </th>
<th>Description
          </th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/3cd9b27d-ceb4-4655-ab3f-3d341774c81a">CreatePartnershipComplete</a>
</td>
<td>Occurs when an asynchronous call to <b>IWMPSyncDevice::createPartnership</b> completes.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/ed726579-e0cb-4007-98eb-b6df4b636b12">DeviceConnect</a>
</td>
<td>Occurs when the user connects a device to the computer.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/a37b72f9-4f71-433c-afad-66caae2d749a">DeviceDisconnect</a>
</td>
<td>Occurs when the user disconnects a device from the computer.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/f9781dde-e813-4e2d-820d-5a0803bfbe4e">DeviceStatusChange</a>
</td>
<td>Occurs when the partnership status of a device changes.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/41e9a6df-3721-4fd2-aa9d-9874a004aa9a">DeviceSyncError</a>
</td>
<td>Occurs when a synchronization error happens.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/98970d33-8035-49f9-9243-b4832df6e5c9">DeviceSyncStateChange</a>
</td>
<td>Occurs when the synchronization state of a device changes.</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5d9eb1c7-7022-4442-b67a-6a96fe5ce97f">Handling Events in C++</a>



<a href="https://msdn.microsoft.com/396545d5-8844-4dd2-9ed5-e4ed77f352ac">IWMPEvents Interface</a>



<a href="https://msdn.microsoft.com/734a8717-3b7f-4a40-895f-b55cfabd665c">IWMPSyncDevice::createPartnership</a>



<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>



<a href="https://msdn.microsoft.com/d543b2a0-a2cb-47e2-b50e-4513fc061b46">Remoting the Windows Media Player Control</a>



<a href="https://msdn.microsoft.com/883d538e-19b6-417b-a32d-622c41c24b9c">_WMPOCXEvents Interface</a>
 

 

