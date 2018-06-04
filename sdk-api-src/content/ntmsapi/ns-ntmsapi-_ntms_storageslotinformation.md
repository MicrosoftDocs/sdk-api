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

# _NTMS_STORAGESLOTINFORMATION structure


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>NTMS_STORAGESLOTINFORMATION</b> structure defines properties specific to a storage slot object.


## -struct-fields




### -field Number

Number of the slot in the library.


### -field State

Current state of the slot. This can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_SLOTSTATE_EMPTY"></a><a id="ntms_slotstate_empty"></a><dl>
<dt><b>NTMS_SLOTSTATE_EMPTY</b></dt>
</dl>
</td>
<td width="60%">
Slot is present, but does not contain a piece of physical media.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_SLOTSTATE_FULL"></a><a id="ntms_slotstate_full"></a><dl>
<dt><b>NTMS_SLOTSTATE_FULL</b></dt>
</dl>
</td>
<td width="60%">
Slot is present and contains a piece of physical media.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_SLOTSTATE_NOTPRESENT"></a><a id="ntms_slotstate_notpresent"></a><dl>
<dt><b>NTMS_SLOTSTATE_NOTPRESENT</b></dt>
</dl>
</td>
<td width="60%">
Slot is not present. If the library contains magazines, this value is reported for each slot when the associated magazine is missing.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_SLOTSTATE_UNKNOWN"></a><a id="ntms_slotstate_unknown"></a><dl>
<dt><b>NTMS_SLOTSTATE_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
Slot state cannot be determined.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_SLOTSTATE_NEEDSINVENTORY"></a><a id="ntms_slotstate_needsinventory"></a><dl>
<dt><b>NTMS_SLOTSTATE_NEEDSINVENTORY</b></dt>
</dl>
</td>
<td width="60%">
Slot needs inventory.

</td>
</tr>
</table>
 


### -field Library

Library that contains the slot.


## -remarks



The 
<b>NTMS_STORAGESLOTINFORMATION</b> structure is part of the 
<a href="https://msdn.microsoft.com/56e3380b-47c7-4861-bb2b-31d67ac10fe1">NTMS_OBJECTINFORMATION</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/56e3380b-47c7-4861-bb2b-31d67ac10fe1">NTMS_OBJECTINFORMATION</a>
 

 

