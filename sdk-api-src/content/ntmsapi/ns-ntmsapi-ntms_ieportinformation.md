---
UID: NS:ntmsapi._NTMS_IEPORTINFORMATION
title: NTMS_IEPORTINFORMATION (ntmsapi.h)
author: windows-sdk-content
description: The NTMS_IEPORTINFORMATION structure defines properties specific to an insert/eject port object.
old-location: fs\ntms_ieportinformation.htm
tech.root: Rsm
ms.assetid: e932a482-12d8-4fb2-bbbc-0e0cf6ee0b42
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: NTMS_IEPORTINFORMATION, NTMS_IEPORTINFORMATION structure [Files], NTMS_PORTCONTENT_EMPTY, NTMS_PORTCONTENT_FULL, NTMS_PORTCONTENT_UNKNOWN, NTMS_PORTPOSITION_EXTENDED, NTMS_PORTPOSITION_RETRACTED, NTMS_PORTPOSITION_UNKNOWN, _zaw_ntms_ieportinformation, base.ntms_ieportinformation, fs.ntms_ieportinformation, ntmsapi/NTMS_IEPORTINFORMATION
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntmsapi.h
api_name:
 - NTMS_IEPORTINFORMATION
product: Windows
targetos: Windows
req.typenames: NTMS_IEPORTINFORMATION
req.redist: 
---

# NTMS_IEPORTINFORMATION structure


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
 

 

