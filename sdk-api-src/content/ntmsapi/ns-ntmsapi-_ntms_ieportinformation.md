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

# _NTMS_IEPORTINFORMATION structure


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>NTMS_IEPORTINFORMATION</b> structure defines properties specific to an insert/eject port object.


## -struct-fields




### -field Number

Library port number.


### -field Content

Full/Empty state of the NTMS_IEPORT object. This can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_PORTCONTENT_FULL"></a><a id="ntms_portcontent_full"></a><dl>
<dt><b>NTMS_PORTCONTENT_FULL</b></dt>
</dl>
</td>
<td width="60%">
Port is full.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_PORTCONTENT_EMPTY"></a><a id="ntms_portcontent_empty"></a><dl>
<dt><b>NTMS_PORTCONTENT_EMPTY</b></dt>
</dl>
</td>
<td width="60%">
Port is empty.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_PORTCONTENT_UNKNOWN"></a><a id="ntms_portcontent_unknown"></a><dl>
<dt><b>NTMS_PORTCONTENT_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
Content of port is not known.

</td>
</tr>
</table>
 


### -field Position

Position of the NTMS_IEPORT object. This can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_PORTPOSITION_EXTENDED"></a><a id="ntms_portposition_extended"></a><dl>
<dt><b>NTMS_PORTPOSITION_EXTENDED</b></dt>
</dl>
</td>
<td width="60%">
Port is extended.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_PORTPOSITION_RETRACTED"></a><a id="ntms_portposition_retracted"></a><dl>
<dt><b>NTMS_PORTPOSITION_RETRACTED</b></dt>
</dl>
</td>
<td width="60%">
Port is retracted.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_PORTPOSITION_UNKNOWN"></a><a id="ntms_portposition_unknown"></a><dl>
<dt><b>NTMS_PORTPOSITION_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
Port position is unknown.

</td>
</tr>
</table>
 


### -field MaxExtendSecs

Maximum number of seconds the port is allowed to remain open before an operator request is issued. Valid values are between 0 and 65,535 seconds. This member is writable.


### -field Library

Library that contains the port.


## -remarks



The 
<b>NTMS_IEPORTINFORMATION</b> structure is included in the 
<a href="https://msdn.microsoft.com/56e3380b-47c7-4861-bb2b-31d67ac10fe1">NTMS_OBJECTINFORMATION</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/56e3380b-47c7-4861-bb2b-31d67ac10fe1">NTMS_OBJECTINFORMATION</a>
 

 

