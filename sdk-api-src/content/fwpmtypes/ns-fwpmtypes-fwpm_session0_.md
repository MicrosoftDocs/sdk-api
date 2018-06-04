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

# FWPM_SESSION0_ structure


## -description


The <b>FWPM_SESSION0</b> structure stores the state associated with a client session.


## -struct-fields




### -field sessionKey

Uniquely identifies the session. 

If this member is zero in the
   call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff550075">FwpmEngineOpen0</a>, Base Filtering Engine (BFE) will generate a GUID.


### -field displayData

Allows sessions to be annotated in a human-readable form.

See <a href="https://msdn.microsoft.com/library/windows/hardware/ff550081">FWPM_DISPLAY_DATA0</a> for more information.


### -field flags

Settings to control session behavior.

<table>
<tr>
<th>Session flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FWPM_SESSION_FLAG_DYNAMIC"></a><a id="fwpm_session_flag_dynamic"></a><dl>
<dt><b>FWPM_SESSION_FLAG_DYNAMIC</b></dt>
</dl>
</td>
<td width="60%">
When this flag is set, any objects added during the session are
automatically deleted when the session ends.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_SESSION_FLAG_RESERVED"></a><a id="fwpm_session_flag_reserved"></a><dl>
<dt><b>FWPM_SESSION_FLAG_RESERVED</b></dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
</table>
 


### -field txnWaitTimeoutInMSec

Time in milli-seconds that a client will wait to begin a transaction. 

If this member is zero, BFE will use a
   default timeout.


### -field processId

Process ID of the client.


### -field sid

SID of the client.


### -field username

User name of the client.


### -field kernelMode

TRUE if this is a kernel-mode client.


## -remarks



This structure contains information supplied by the client when creating a session by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff550075">FwpmEngineOpen0</a>, or information retrieved from the system when enumerating sessions by calling <a href="https://msdn.microsoft.com/fb67d74a-dd96-434c-b218-a34ca6043cb1">FwpmSessionEnum0</a>.

The members <b>processId</b>, <b>sid</b>,  <b>username</b>, and <b>kernelMode</b> are not supplied by the client. They are supplied by BFE and can be retrieved when enumerating sessions.

<b>FWPM_SESSION0</b> is a specific implementation of FWPM_SESSION. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550081">FWPM_DISPLAY_DATA0</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550075">FwpmEngineOpen0</a>



<a href="https://msdn.microsoft.com/fb67d74a-dd96-434c-b218-a34ca6043cb1">FwpmSessionEnum0</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

