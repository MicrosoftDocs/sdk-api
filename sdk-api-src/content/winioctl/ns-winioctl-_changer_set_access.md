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

# _CHANGER_SET_ACCESS structure


## -description


Contains information that the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff559422">IOCTL_CHANGER_SET_ACCESS</a> control code needs to set the state of the device's insert/eject port, door, or keypad.


## -struct-fields




### -field Element

A 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff551457">CHANGER_ELEMENT</a> structure that represents the changer element. The <b>ElementType</b> member can be one of the following values: ChangerDoor, ChangerIEPort, or ChangerKeypad.


### -field Control

The operation to be performed.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EXTEND_IEPORT"></a><a id="extend_ieport"></a><dl>
<dt><b>EXTEND_IEPORT</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The element is to be extended. 




Requires that <b>Features0</b> is CHANGER_OPEN_IEPORT.

</td>
</tr>
<tr>
<td width="40%"><a id="LOCK_ELEMENT"></a><a id="lock_element"></a><dl>
<dt><b>LOCK_ELEMENT</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The element is to be locked. 




Requires that <b>Features0</b> is CHANGER_LOCK_UNLOCK.

</td>
</tr>
<tr>
<td width="40%"><a id="RETRACT_IEPORT"></a><a id="retract_ieport"></a><dl>
<dt><b>RETRACT_IEPORT</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The element is to be retracted. 




Requires that <b>Features0</b> is CHANGER_CLOSE_IEPORT.

</td>
</tr>
<tr>
<td width="40%"><a id="UNLOCK_ELEMENT"></a><a id="unlock_element"></a><dl>
<dt><b>UNLOCK_ELEMENT</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The element is to be unlocked. 




Requires that <b>Features0</b> is CHANGER_LOCK_UNLOCK.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551457">CHANGER_ELEMENT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559422">IOCTL_CHANGER_SET_ACCESS</a>
 

 

