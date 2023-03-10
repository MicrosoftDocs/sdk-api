---
UID: NS:nb30._NCB
title: NCB (nb30.h)
description: The NCB structure represents a network control block.
helpviewer_keywords: ["*PNCB","NCB","NCB structure [NetBIOS]","PNCB","PNCB structure pointer [NetBIOS]","nb30/NCB","nb30/PNCB","netbios.ncb"]
old-location: netbios\ncb.htm
tech.root: NetBIOS
ms.assetid: e3fcca1c-8057-41c4-80a5-d1e67920d88c
ms.date: 12/05/2018
ms.keywords: '*PNCB, NCB, NCB structure [NetBIOS], PNCB, PNCB structure pointer [NetBIOS], nb30/NCB, nb30/PNCB, netbios.ncb'
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
targetos: Windows
req.typenames: NCB, *PNCB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NCB
 - nb30/_NCB
 - PNCB
 - nb30/PNCB
 - NCB
 - nb30/NCB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Nb30.h
api_name:
 - NCB
---

# NCB structure


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/netbios/portal">Netbios</a> is not supported on Windows Vista,  Windows Server 2008, and subsequent versions of the operating system]

The <b>NCB</b> structure represents a network control block. It contains information about the command to perform, an optional post routine, an optional event handle, and a pointer to a buffer that is used for messages or other data. A pointer to this structure is passed to the <a href="/previous-versions/windows/desktop/api/nb30/nf-nb30-netbios">Netbios</a> function.

## -struct-fields

### -field ncb_command

Specifies the command code and a flag that indicates whether the <b>NCB</b> structure is processed asynchronously. The most significant bit contains the flag. If the ASYNCH constant is combined with a command code (by using the OR operator), the <b>NCB</b> structure is processed asynchronously. The following command codes are supported.

<table>
<tr>
<th>Code</th>
<th>Meaning</th>
</tr>
<tr>
<td>NCBACTION</td>
<td>

<b>Windows Server 2003, Windows XP, Windows 2000, and Windows NT:  </b>Enables extensions to the transport interface. NCBACTION is mapped to <b>TdiAction</b>. When this code is specified, the <b>ncb_buffer</b> member points to a buffer to be filled with an <a href="/windows/desktop/api/nb30/ns-nb30-action_header">ACTION_HEADER</a> structure, which is optionally followed by data. NCBACTION commands cannot be canceled by using NCBCANCEL. 
NCBACTION is not a standard NetBIOS 3.0 command.



</td>
</tr>
<tr>
<td>NCBADDGRNAME  
</td>
<td>
Adds a group name to the local name table. This name cannot be used by another process on the network as a unique name, but it can be added by anyone as a group name.

</td>
</tr>
<tr>
<td>NCBADDNAME</td>
<td>
Adds a unique name to the local name table. The TDI driver ensures that the name is unique across the network.

</td>
</tr>
<tr>
<td>NCBASTAT</td>
<td>
Retrieves the status of either a local or remote adapter. When this code is specified, the <b>ncb_buffer</b> member points to a buffer to be filled with an <a href="/windows/desktop/api/nb30/ns-nb30-adapter_status">ADAPTER_STATUS</a> structure, followed by an array of <a href="/windows/desktop/api/nb30/ns-nb30-name_buffer">NAME_BUFFER</a> structures.

</td>
</tr>
<tr>
<td>NCBCALL</td>
<td>
Opens a session with another name.

</td>
</tr>
<tr>
<td>NCBCANCEL</td>
<td>
Cancels a previous pending command.

</td>
</tr>
<tr>
<td>NCBCHAINSEND</td>
<td>
Sends the contents of two data buffers to the specified session partner.

</td>
</tr>
<tr>
<td>NCBCHAINSENDNA</td>
<td>
Sends the contents of two data buffers to the specified session partner and does not wait for acknowledgment. 

</td>
</tr>
<tr>
<td>NCBDELNAME</td>
<td>
Deletes a name from the local name table.

</td>
</tr>
<tr>
<td>NCBDGRECV</td>
<td>
Receives a datagram from any name.

</td>
</tr>
<tr>
<td>NCBDGRECVBC</td>
<td>
Receives a broadcast datagram from any name.

</td>
</tr>
<tr>
<td>NCBDGSEND</td>
<td>
Sends datagram to a specified name.

</td>
</tr>
<tr>
<td>NCBDGSENDBC</td>
<td>
Sends a broadcast datagram to every host on the local area network (LAN).

</td>
</tr>
<tr>
<td>NCBENUM</td>
<td>

<b>Windows Server 2003, Windows XP, Windows 2000, and Windows NT:  </b>Enumerates LAN adapter (LANA) numbers. When this code is specified, the ncb_buffer member points to a buffer to be filled with a LANA_ENUM structure. NCBENUM is not a standard NetBIOS 3.0 command. 




</td>
</tr>
<tr>
<td>NCBFINDNAME</td>
<td>
Determines the location of a name on the network. When this code is specified, the <b>ncb_buffer</b> member points to a buffer to be filled with a <a href="/windows/desktop/api/nb30/ns-nb30-find_name_header">FIND_NAME_HEADER</a> structure followed by one or more <a href="/windows/desktop/api/nb30/ns-nb30-find_name_buffer">FIND_NAME_BUFFER</a> structures.

</td>
</tr>
<tr>
<td>NCBHANGUP</td>
<td>
Closes a specified session.

</td>
</tr>
<tr>
<td>NCBLANSTALERT</td>
<td>

<b>Windows Server 2003, Windows XP, Windows 2000, and Windows NT:  </b>Notifies the user of LAN failures that last for more than one minute.



</td>
</tr>
<tr>
<td>NCBLISTEN</td>
<td>
Enables a session to be opened with another name (local or remote).

</td>
</tr>
<tr>
<td>NCBRECV</td>
<td>
Receives data from the specified session partner.

</td>
</tr>
<tr>
<td>NCBRECVANY</td>
<td>
Receives data from any session corresponding to a specified name.

</td>
</tr>
<tr>
<td>NCBRESET</td>
<td>
Resets a LAN adapter. An adapter must be reset before it can accept any other NCB command that specifies the same number in the <b>ncb_lana_num</b> member.

Use the following values to specify how resources are to be freed:


<ul>
<li>If <b>ncb_lsn</b> is not 0x00, all resources associated with <b>ncb_lana_num</b> are to be freed.</li>
<li>If <b>ncb_lsn</b> is 0x00, all resources associated with <b>ncb_lana_num</b> are to be freed, and new resources are to be allocated. The <b>ncb_callname</b>[0] byte specifies the maximum number of sessions, and the <b>ncb_callname</b>[2] byte specifies the maximum number of names. A nonzero value for the <b>ncb_callname</b>[3] byte requests that the application use <b>NAME_NUMBER_1</b>.  
</li>
</ul>


</td>
</tr>
<tr>
<td>NCBSEND</td>
<td>
Sends data to the specified session partner. 

</td>
</tr>
<tr>
<td>NCBSENDNA</td>
<td>
Sends data to specified session partner and does not wait for acknowledgment. 

</td>
</tr>
<tr>
<td>NCBSSTAT</td>
<td>
Retrieves the status of the session. When this value is specified, the <b>ncb_buffer</b> member points to a buffer to be filled with a <a href="/windows/desktop/api/nb30/ns-nb30-session_header">SESSION_HEADER</a> structure, followed by one or more <a href="/windows/desktop/api/nb30/ns-nb30-session_buffer">SESSION_BUFFER</a> structures.

</td>
</tr>
<tr>
<td>NCBTRACE</td>
<td>
Activates or deactivates NCB tracing. 

This command is not supported. 


</td>
</tr>
<tr>
<td>NCBUNLINK</td>
<td>
Unlinks the adapter.

This command is provided for compatibility with earlier versions of NetBIOS. It has no effect in Windows.

</td>
</tr>
</table>

### -field ncb_retcode

Specifies the return code. This value is set to NRC_PENDING while an asynchronous operation is in progress. The system returns one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>NRC_GOODRET</td>
<td>The operation succeeded.</td>
</tr>
<tr>
<td>NRC_BUFLEN</td>
<td>An illegal buffer length was supplied.</td>
</tr>
<tr>
<td>NRC_ILLCMD</td>
<td>An illegal command was supplied.</td>
</tr>
<tr>
<td>NRC_CMDTMO</td>
<td>The command was timed out.</td>
</tr>
<tr>
<td>NRC_INCOMP</td>
<td>The message was incomplete. The application is to issue another command.</td>
</tr>
<tr>
<td>NRC_BADDR</td>
<td>The buffer address was illegal.</td>
</tr>
<tr>
<td>NRC_SNUMOUT</td>
<td>The session number was out of range.</td>
</tr>
<tr>
<td>NRC_NORES</td>
<td>No resource was available.</td>
</tr>
<tr>
<td>NRC_SCLOSED</td>
<td>The session was closed.</td>
</tr>
<tr>
<td>NRC_CMDCAN</td>
<td>The command was canceled.</td>
</tr>
<tr>
<td>NRC_DUPNAME</td>
<td>A duplicate name existed in the local name table.</td>
</tr>
<tr>
<td>NRC_NAMTFUL</td>
<td>The name table was full.</td>
</tr>
<tr>
<td>NRC_ACTSES</td>
<td>The command finished; the name has active sessions and is no longer registered.</td>
</tr>
<tr>
<td>NRC_LOCTFUL</td>
<td>The local session table was full.</td>
</tr>
<tr>
<td>NRC_REMTFUL</td>
<td>The remote session table was full. The request to open a session was rejected.</td>
</tr>
<tr>
<td>NRC_ILLNN</td>
<td>An illegal name number was specified.</td>
</tr>
<tr>
<td>NRC_NOCALL</td>
<td>The system did not find the name that was called.</td>
</tr>
<tr>
<td>NRC_NOWILD</td>
<td>Wildcards are not permitted in the <b>ncb_name</b> member.</td>
</tr>
<tr>
<td>NRC_INUSE</td>
<td>The name was already in use on the remote adapter.</td>
</tr>
<tr>
<td>NRC_NAMERR</td>
<td>The name was deleted.</td>
</tr>
<tr>
<td>NRC_SABORT</td>
<td>The session ended abnormally.</td>
</tr>
<tr>
<td>NRC_NAMCONF</td>
<td>A name conflict was detected.</td>
</tr>
<tr>
<td>NRC_IFBUSY</td>
<td>The interface was busy.</td>
</tr>
<tr>
<td>NRC_TOOMANY</td>
<td>Too many commands were outstanding; the application can retry the command later.</td>
</tr>
<tr>
<td>NRC_BRIDGE</td>
<td>The <b>ncb_lana_num</b> member did not specify a valid network number.</td>
</tr>
<tr>
<td>NRC_CANOCCR</td>
<td>The command finished while a cancel operation was occurring.</td>
</tr>
<tr>
<td>NRC_CANCEL</td>
<td>The NCBCANCEL command was not valid; the command was not canceled.</td>
</tr>
<tr>
<td>NRC_DUPENV</td>
<td>The name was defined by another local process.</td>
</tr>
<tr>
<td>NRC_ENVNOTDEF</td>
<td>The environment was not defined. A reset command must be issued.</td>
</tr>
<tr>
<td>NRC_OSRESNOTAV</td>
<td>Operating system resources were exhausted. The application can retry the command later.</td>
</tr>
<tr>
<td>NRC_MAXAPPS</td>
<td>The maximum number of applications was exceeded.</td>
</tr>
<tr>
<td>NRC_NOSAPS</td>
<td>No service access points (SAPs) were available for NetBIOS.</td>
</tr>
<tr>
<td>NRC_NORESOURCES</td>
<td>The requested resources were not available.</td>
</tr>
<tr>
<td>NRC_INVADDRESS</td>
<td>The NCB address was not valid.</td>
</tr>
<tr>
<td>NRC_INVDDID</td>
<td>
The NCB DDID was invalid.

This return code is not part of the IBM NetBIOS 3.0 specification and is not returned in the <b>NCB</b> structure. Instead, it is returned by the <a href="/previous-versions/windows/desktop/api/nb30/nf-nb30-netbios">Netbios</a> function.

</td>
</tr>
<tr>
<td>NRC_LOCKFAIL</td>
<td>The attempt to lock the user area failed.</td>
</tr>
<tr>
<td>NRC_OPENERR</td>
<td>An error occurred during an open operation being performed by the device driver. This error code is not part of the NetBIOS 3.0 specification.</td>
</tr>
<tr>
<td>NRC_SYSTEM</td>
<td>A system error occurred.</td>
</tr>
<tr>
<td>NRC_PENDING</td>
<td>An asynchronous operation is not yet finished.</td>
</tr>
</table>

### -field ncb_lsn

Identifies the local session number. This number uniquely identifies a session within an environment. This number is returned by the <a href="/previous-versions/windows/desktop/api/nb30/nf-nb30-netbios">Netbios</a> function after a successful NCBCALL command.

### -field ncb_num

Specifies the number for the local network name. This number is returned by <a href="/previous-versions/windows/desktop/api/nb30/nf-nb30-netbios">Netbios</a> after a successful <b>NCBADDNAME</b> or <b>NCBADDGRNAME</b> command. This number, not the name, must be used with all datagram commands and for <b>NCBRECVANY</b> commands.

The number for <b>NAME_NUMBER_1</b> is always 0x01. The <a href="/previous-versions/windows/desktop/api/nb30/nf-nb30-netbios">Netbios</a> function assigns values in the range 0x02 to 0xFE for the remaining names.

### -field ncb_buffer

Pointer to the message buffer. The buffer must have write access. Its uses are as follows:

<table>
<tr>
<th>Command</th>
<th>Purpose</th>
</tr>
<tr>
<td>NCBSEND</td>
<td>Contains the message to be sent. </td>
</tr>
<tr>
<td>NCBRECV</td>
<td>Receives the message. </td>
</tr>
<tr>
<td>NCBSSTAT</td>
<td>Receives the requested status information.</td>
</tr>
</table>

### -field ncb_length

Specifies the size, in bytes, of the message buffer. For receive commands, this member is set by the <a href="/previous-versions/windows/desktop/api/nb30/nf-nb30-netbios">Netbios</a> function to indicate the number of bytes received.

If the buffer length is incorrect, the <a href="/previous-versions/windows/desktop/api/nb30/nf-nb30-netbios">Netbios</a> function returns the <b>NRC_BUFLEN</b> error code.

### -field ncb_callname

Specifies the name of the remote application. Trailing-space characters should be supplied to make the length of the string equal to <b>NCBNAMSZ</b>.

### -field ncb_name

Specifies the name by which the application is known. Trailing-space characters should be supplied to make the length of the string equal to <b>NCBNAMSZ</b>.

### -field ncb_rto

Specifies the time-out period for receive operations, in 500-millisecond units, for the session. A value of zero implies no time-out. Specify with the <b>NCBCALL</b> or <b>NCBLISTEN</b> command. Affects subsequent <b>NCBRECV</b> commands.

### -field ncb_sto

Specifies the time-out period for send operations, in 500-millisecond units, for the session. A value of zero implies no time-out. Specify with the <b>NCBCALL</b> or <b>NCBLISTEN</b> command. Affects subsequent <b>NCBSEND</b> and <b>NCBCHAINSEND</b> commands.

### -field ncb_post

Specifies the address of the post routine to call when the asynchronous command is completed. The post routine is defined as:

  NCB_POST PostRoutine( PNCB <i>pncb</i> );

where the <i>pncb</i> parameter is a pointer to the completed <b>NCB</b> structure.

### -field ncb_lana_num

Specifies the LAN adapter number. This zero-based number corresponds to a particular transport provider using a particular LAN adapter board.

### -field ncb_cmd_cplt

Specifies the command complete flag. This value is the same as the <b>ncb_retcode</b> member.

### -field ncb_reserve

Reserved; must be zero.

The length, X,  of the <b>ncb_reserve</b>  array is dependent upon the system architecture. For 64-bit systems, the  array contains 18 elements. Otherwise, the array contains 10 elements.

### -field ncb_event

Specifies a handle to an event object that is set to the nonsignaled state when an asynchronous command is accepted, and it is set to the signaled state when the asynchronous command is completed. The event is signaled if the <a href="/previous-versions/windows/desktop/api/nb30/nf-nb30-netbios">Netbios</a> function returns a nonzero value. Only manual reset events should be used for synchronization. A specified event should not be associated with more than one active asynchronous command.

The <b>ncb_event</b> member must be zero if the <b>ncb_command</b> member does not have the <b>ASYNCH</b> flag set or if <b>ncb_post</b> is nonzero. Otherwise, <a href="/previous-versions/windows/desktop/api/nb30/nf-nb30-netbios">Netbios</a> returns the <b>NRC_ILLCMD</b> error code.

## -remarks

Using <b>ncb_event</b> to issue asynchronous requests requires fewer system resources than using <b>ncb_post</b>. In addition, when <b>ncb_event</b> is nonzero, the pending request is canceled if the thread terminates before the request is processed. This is not true for asynchronous requests sent using <b>ncb_post</b>.

## -see-also

<b></b>



<a href="/windows/desktop/api/nb30/ns-nb30-action_header">ACTION_HEADER</a>



<a href="/windows/desktop/api/nb30/ns-nb30-adapter_status">ADAPTER_STATUS</a>



<a href="/windows/desktop/api/nb30/ns-nb30-find_name_buffer">FIND_NAME_BUFFER</a>



<a href="/windows/desktop/api/nb30/ns-nb30-find_name_header">FIND_NAME_HEADER</a>



<a href="/windows/desktop/api/nb30/ns-nb30-lana_enum">LANA_ENUM</a>



<a href="/windows/desktop/api/nb30/ns-nb30-name_buffer">NAME_BUFFER</a>



<a href="/previous-versions/windows/desktop/netbios/netbios-structures">NetBIOS Structures</a>



<a href="/previous-versions/windows/desktop/api/nb30/nf-nb30-netbios">Netbios</a>



<a href="/windows/desktop/api/nb30/ns-nb30-session_buffer">SESSION_BUFFER</a>



<a href="/windows/desktop/api/nb30/ns-nb30-session_header">SESSION_HEADER</a>



<a href="/previous-versions/windows/desktop/netbios/portal">The NetBIOS Interface Overview</a>