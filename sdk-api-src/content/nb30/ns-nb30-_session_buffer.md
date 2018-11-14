---
UID: NS:nb30._SESSION_BUFFER
title: "_SESSION_BUFFER"
author: windows-sdk-content
description: The SESSION_BUFFER structure contains information about a local network session. One or more SESSION_BUFFER structures follows a SESSION_HEADER structure when an application specifies the NCBSSTAT command in the ncb_command member of the NCB structure.
old-location: netbios\session_buffer.htm
tech.root: NetBIOS
ms.assetid: 29352074-3dff-430f-82fb-6f7fd0b2966a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PSESSION_BUFFER, CALL_PENDING, HANGUP_COMPLETE, HANGUP_PENDING, LISTEN_OUTSTANDING, PSESSION_BUFFER, PSESSION_BUFFER structure pointer [NetBIOS], SESSION_ABORTED, SESSION_BUFFER, SESSION_BUFFER structure [NetBIOS], SESSION_ESTABLISHED, _SESSION_BUFFER, nb30/PSESSION_BUFFER, nb30/SESSION_BUFFER, netbios.session_buffer"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: nb30.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Nb30.h
api_name:
 - SESSION_BUFFER
product: Windows
targetos: Windows
req.typenames: SESSION_BUFFER, *PSESSION_BUFFER
req.redist: 
---

# _SESSION_BUFFER structure


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/9144e283-0e5f-43d7-8cd2-e746f94c6f14">Netbios</a> is not supported on Windows Vista,  Windows Server 2008, and subsequent versions of the operating system]

The <b>SESSION_BUFFER</b> structure contains information about a local network session. One or more <b>SESSION_BUFFER</b> structures follows a <a href="https://msdn.microsoft.com/0b466bc7-6d20-477f-9e64-1d3dc0744484">SESSION_HEADER</a> structure when an application specifies the <b>NCBSSTAT</b> command in the <b>ncb_command</b> member of the <a href="https://msdn.microsoft.com/e3fcca1c-8057-41c4-80a5-d1e67920d88c">NCB</a> structure. 




## -struct-fields




### -field lsn

Specifies the local session number.


### -field state

Specifies the state of the session. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LISTEN_OUTSTANDING"></a><a id="listen_outstanding"></a><dl>
<dt><b>LISTEN_OUTSTANDING</b></dt>
</dl>
</td>
<td width="60%">
The session is waiting for a call from a remote computer.

</td>
</tr>
<tr>
<td width="40%"><a id="CALL_PENDING"></a><a id="call_pending"></a><dl>
<dt><b>CALL_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The session is attempting to connect to a remote computer.

</td>
</tr>
<tr>
<td width="40%"><a id="SESSION_ESTABLISHED"></a><a id="session_established"></a><dl>
<dt><b>SESSION_ESTABLISHED</b></dt>
</dl>
</td>
<td width="60%">
The session connected and is able to transfer data.

</td>
</tr>
<tr>
<td width="40%"><a id="HANGUP_PENDING"></a><a id="hangup_pending"></a><dl>
<dt><b>HANGUP_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The session is being deleted due to a command by the local user.

</td>
</tr>
<tr>
<td width="40%"><a id="HANGUP_COMPLETE"></a><a id="hangup_complete"></a><dl>
<dt><b>HANGUP_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The session was deleted due to a command by the local user.

</td>
</tr>
<tr>
<td width="40%"><a id="SESSION_ABORTED"></a><a id="session_aborted"></a><dl>
<dt><b>SESSION_ABORTED</b></dt>
</dl>
</td>
<td width="60%">
The session was abandoned due to a network or user problem.

</td>
</tr>
</table>
 


### -field local_name

Specifies the 16-byte NetBIOS name on the local computer used for this session.


### -field remote_name

 


### -field rcvs_outstanding

Specifies the number of pending <b>NCBRECV</b> commands.


### -field sends_outstanding

Specifies the number of pending <b>NCBSEND</b> and <b>NCBCHAINSEND</b> commands.


#### - Remote_name

Specifies the 16-byte NetBIOS name on the remote computer used for this session.


## -see-also




<b></b>



<a href="https://msdn.microsoft.com/e3fcca1c-8057-41c4-80a5-d1e67920d88c">NCB</a>



<a href="https://msdn.microsoft.com/64ef39ec-d69a-4e33-9192-dda6d1bb84b8">NetBIOS Structures</a>



<a href="https://msdn.microsoft.com/0b466bc7-6d20-477f-9e64-1d3dc0744484">SESSION_HEADER</a>



<a href="https://msdn.microsoft.com/9144e283-0e5f-43d7-8cd2-e746f94c6f14">The NetBIOS Interface Overview</a>
 

 

