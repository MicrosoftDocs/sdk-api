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

# _NTMS_IEDOORINFORMATION structure


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>NTMS_IEDOORINFORMATION</b> structure defines properties specific to an insert/eject door object.


## -struct-fields




### -field Number

Number of the door in the library. Typically, libraries have one door.


### -field State

State of the door. This can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_DOORSTATE_CLOSED"></a><a id="ntms_doorstate_closed"></a><dl>
<dt><b>NTMS_DOORSTATE_CLOSED</b></dt>
</dl>
</td>
<td width="60%">
Library door is closed.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_DOORSTATE_OPEN"></a><a id="ntms_doorstate_open"></a><dl>
<dt><b>NTMS_DOORSTATE_OPEN</b></dt>
</dl>
</td>
<td width="60%">
Library door is open.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_DOORSTATE_UNKNOWN"></a><a id="ntms_doorstate_unknown"></a><dl>
<dt><b>NTMS_DOORSTATE_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
State of the library is unknown.

</td>
</tr>
</table>
 


### -field MaxOpenSecs

Maximum number of seconds the door is to remain open. Valid values are between 0-65,535 seconds This member is writable.


### -field Library

Library that contains this door.


## -remarks



The 
<b>NTMS_IEDOORINFORMATION</b> structure is included in the 
<a href="https://msdn.microsoft.com/56e3380b-47c7-4861-bb2b-31d67ac10fe1">NTMS_OBJECTINFORMATION</a> structure.

If the <b>MaxOpenSecs</b> member is zero, an operator request to close the door is generated as soon as the door is open.




## -see-also




<a href="https://msdn.microsoft.com/56e3380b-47c7-4861-bb2b-31d67ac10fe1">NTMS_OBJECTINFORMATION</a>
 

 

