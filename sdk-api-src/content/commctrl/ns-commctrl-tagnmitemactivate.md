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

# tagNMITEMACTIVATE structure


## -description


Contains information about an <a href="https://msdn.microsoft.com/475c8e6a-8e2e-4182-8ccc-a4bc6fc891a8">LVN_ITEMACTIVATE</a> notification code. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains information about this notification code. 


### -field iItem

Type: <b>int</b>

Index of the list-view item. If the item index is not used for the notification, this member will contain -1. 


### -field iSubItem

Type: <b>int</b>

One-based index of the subitem. If the subitem index is not used for the notification or the notification does not apply to a subitem, this member will contain zero. 


### -field uNewState

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

New item state. This member is zero for notification codes that do not use it. 


### -field uOldState

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Old item state. This member is zero for notification codes that do not use it. 


### -field uChanged

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Set of flags that indicate the item attributes that have changed. This member is zero for notifications that do not use it. Otherwise, it can have the same values as the 
					<b>mask</b> member of the <a href="https://msdn.microsoft.com/4141a2ee-9016-4d76-8758-a36fc6eedb44">LVITEM</a> structure. 


### -field ptAction

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a></b>


<a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure that indicates the location at which the event occurred, in client coordinates. This member is undefined for notification codes that do not use it. 


### -field lParam

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

Application-defined value of the item. This member is undefined for notification codes that do not use it. 


### -field uKeyFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Modifier keys that were pressed at the time of the activation. This member contains zero or a combination of the following flags: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LVKF_ALT"></a><a id="lvkf_alt"></a><dl>
<dt><b>LVKF_ALT</b></dt>
</dl>
</td>
<td width="60%">
The  key is pressed. 

</td>
</tr>
<tr>
<td width="40%"><a id="LVKF_CONTROL"></a><a id="lvkf_control"></a><dl>
<dt><b>LVKF_CONTROL</b></dt>
</dl>
</td>
<td width="60%">
The  key is pressed. 

</td>
</tr>
<tr>
<td width="40%"><a id="LVKF_SHIFT"></a><a id="lvkf_shift"></a><dl>
<dt><b>LVKF_SHIFT</b></dt>
</dl>
</td>
<td width="60%">
The  key is pressed. 

</td>
</tr>
</table>
 

