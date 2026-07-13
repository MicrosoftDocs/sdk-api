---
UID: NF:icmpapi.Icmp6SendEcho2
title: Icmp6SendEcho2 function (icmpapi.h)
description: The Icmp6SendEcho2 function sends an IPv6 ICMPv6 echo request and returns either immediately (if Event or ApcRoutine is non-NULL) or returns after the specified time-out. The ReplyBuffer contains the IPv6 ICMPv6 echo response, if any.
helpviewer_keywords: ["Icmp6SendEcho2","Icmp6SendEcho2 function [IP Helper]","icmpapi/Icmp6SendEcho2","iphlp.icmp6sendecho2"]
old-location: iphlp\icmp6sendecho2.htm
tech.root: IpHlp
ms.assetid: 622c769b-ede8-4bc2-ac54-98de47ae1fed
ms.date: 10/10/2023
ms.keywords: Icmp6SendEcho2, Icmp6SendEcho2 function [IP Helper], icmpapi/Icmp6SendEcho2, iphlp.icmp6sendecho2
req.header: icmpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Icmp6SendEcho2
 - icmpapi/Icmp6SendEcho2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - Icmp6SendEcho2
---

## -description

The <b>Icmp6SendEcho2</b> function sends an IPv6 ICMPv6 echo request and returns either immediately (if <i>Event</i> or <i>ApcRoutine</i> is non-<b>NULL</b>) or returns after the specified time-out. The <i>ReplyBuffer</i> contains the IPv6 ICMPv6 echo response, if any.

## -parameters

### -param IcmpHandle [in]

The open handle returned by <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6createfile">Icmp6CreateFile</a>.

### -param Event [in, optional]

An event to be signaled whenever an ICMPv6 response arrives. If this parameter is specified, it requires a handle to a valid event object. Use the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> or <a href="/windows/desktop/api/synchapi/nf-synchapi-createeventexa">CreateEventEx</a> function to create this event object. 

For more information on using events, see <a href="/windows/desktop/Sync/event-objects">Event Objects</a>.

### -param ApcRoutine [in, optional]

The routine that is called when the calling thread is in an alertable thread and  an ICMPv6 reply arrives. On Windows Vista and later, <b>PIO_APC_ROUTINE_DEFINED</b> must be defined to force the datatype for this parameter to <b>PIO_APC_ROUTINE</b> rather than <b>FARPROC</b>. 

On Windows Server 2003 and Windows XP, 
   <b>PIO_APC_ROUTINE_DEFINED</b> must not be defined to force the datatype for this parameter to <b>FARPROC</b>.

### -param ApcContext [in, optional]

An optional parameter passed to the callback routine specified in the  <i>ApcRoutine</i> parameter whenever an ICMPv6 response arrives or an error occurs.

### -param SourceAddress [in]

The IPv6 source address on which to issue the echo request, in the form of a <a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure.

### -param DestinationAddress [in]

The IPv6 destination address of the echo request, in the form of a <a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure.

### -param RequestData [in]

A pointer to a buffer that contains data to send in the request.

### -param RequestSize [in]

The size, in bytes, of the request data buffer pointed to by the <i>RequestData</i> parameter.

### -param RequestOptions [in, optional]

A pointer to the IPv6 header options for the request, in the form of an <a href="/windows/desktop/api/ipexport/ns-ipexport-ip_option_information">IP_OPTION_INFORMATION</a> structure. On a 64-bit platform, this parameter is in the form for an <a href="/windows/desktop/api/ipexport/ns-ipexport-ip_option_information32">IP_OPTION_INFORMATION32</a> structure.

This parameter may be NULL if no IP header options need to be specified.

<div class="alert"><b>Note</b>  On Windows Server 2003 and Windows XP, the <i>RequestOptions</i> parameter is not optional and must not be NULL and only the <b>Ttl</b> and <b>Flags</b> members are used.</div>
<div> </div>

### -param ReplyBuffer [out]

A pointer to a buffer to hold replies to the request. Upon return, the buffer contains an <a href="/windows/desktop/api/ipexport/ns-ipexport-icmpv6_echo_reply_lh">ICMPV6_ECHO_REPLY</a> structure followed by the message body from the ICMPv6 echo response reply data. The buffer must be large enough to hold at least one 
<b>ICMPV6_ECHO_REPLY</b> structure plus the number of bytes of data specified in the <i>RequestSize</i> parameter. This buffer should also be large enough to also hold 8 more bytes of data (the size of an ICMP error message) plus space for an <b>IO_STATUS_BLOCK</b> structure.

### -param ReplySize [in]

The size, in bytes,  of the reply buffer pointed to by the <i>ReplyBuffer</i> parameter. This buffer should be large enough to hold at least one 
<a href="/windows/desktop/api/ipexport/ns-ipexport-icmpv6_echo_reply_lh">ICMPV6_ECHO_REPLY</a> structure plus <i>RequestSize</i> bytes of data. This buffer should also be large enough to also hold 8 more bytes of data (the size of an ICMP error message) plus space for an <b>IO_STATUS_BLOCK</b> structure.

### -param Timeout [in]

The time, in milliseconds, to wait for replies. This parameter is only used if the <b>Icmp6SendEcho2</b> function is called synchronously. So this parameter is not used if either the <i>ApcRoutine</i> or <i>Event</i> parameter are not <b>NULL</b>.

## -returns

When called synchronously, returns the number of replies that are received and stored in *ReplyBuffer*.

When called asynchronously, indicates that the operation is in progress by returning **ERROR_IO_PENDING**. You can retrieve the number-of-replies result later, when the event specified in the *Event* parameter signals, or when the callback function in the *ApcRoutine* parameter is called.

If the (synchronous or asynchronous) number-of-replies value is zero, then for extended error information call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

If the function fails, then the extended error code returned by <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> can be one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CALL_NOT_IMPLEMENTED</b></dt>
</dl>
</td>
<td width="60%">
This function is not supported on this system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The data area passed to a system call is too small. This error is returned if the <i>ReplySize</i> parameter indicates that the buffer pointed to by the <i>ReplyBuffer</i> parameter is too small. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid. This error is returned if the <i>IcmpHandle</i> parameter contains an invalid handle. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_IO_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The operation is in progress. This value is returned by a successful asynchronous call to <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6sendecho2">Icmp6SendEcho2</a> and is not an indication of an error.  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory is available to process this command.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if no IPv6 stack is on the local computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IP_BUF_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The size of the <i>ReplyBuffer</i> specified in the <i>ReplySize</i> parameter was too small.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>

## -remarks

The <b>Icmp6SendEcho2</b> function is called synchronously if the <i>ApcRoutine</i> and <i>Event</i> parameters are <b>NULL</b>. When called synchronously, the return value contains the number of replies received and stored in <i>ReplyBuffer</i> after waiting for the time specified in the <i>Timeout</i> parameter. If the return value is zero, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> for extended error information.

The <b>Icmp6SendEcho2</b> function is called asynchronously when either the <i>ApcRoutine</i> or <i>Event</i> parameters are specified. When called asynchronously,  the <i>ReplyBuffer</i> and <i>ReplySize</i> parameters are  required to accept the response. ICMP response data is copied to the <i>ReplyBuffer</i> provided and the application is signaled (when the <i>Event</i> parameter is specified) or the callback function is called (when the <i>ApcRoutine</i> parameter is specified). The application must parse the data pointed to by <i>ReplyBuffer</i> parameter using the <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6parsereplies">Icmp6ParseReplies</a> function. 

If the <i>Event</i> parameter is specified, the <b>Icmp6SendEcho2</b> function is called asynchronously. The event specified in the <i>Event</i> parameter is signaled whenever an ICMPv6 response arrives. Use the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> function to create this event object. 

If the <i>ApcRoutine</i> parameter is specified, the <b>Icmp6SendEcho2</b> function is called asynchronously. The <i>ApcRoutine</i>  parameter should point to a user-defined callback function. The callback function specified in the <i>ApcRoutine</i> parameter is called whenever an ICMPv6 response arrives. The invocation of the callback function specified in the <i>ApcRoutine</i> parameter is serialized. 

If both the <i>Event</i> and <i>ApcRoutine</i> parameters are specified, the event specified in the <i>Event</i> parameter is signaled whenever an ICMPv6 response arrives, but the callback function specified in the <i>ApcRoutine</i> parameter is ignored . 

On Windows Vista and later, any application that calls <b>Icmp6SendEcho2</b> function asynchronously using the <i>ApcRoutine</i> parameter must define <b>PIO_APC_ROUTINE_DEFINED</b> to force the datatype for the <i>ApcRoutine</i> parameter to <b>PIO_APC_ROUTINE</b> rather than <b>FARPROC</b>. <div class="alert"><b>Note</b>  <b>PIO_APC_ROUTINE_DEFINED</b> must be defined before the <i>Icmpapi.h</i> header file is included.</div>
<div> </div>


On Windows Vista and later, the callback function pointed to by the <i>ApcRoutine</i> must be defined as a function of type <b>VOID</b> with the following syntax:


``` syntax
typedef
VOID WINAPI
(*PIO_APC_ROUTINE) (
    IN PVOID ApcContext,
    IN PIO_STATUS_BLOCK IoStatusBlock,
    IN ULONG Reserved
    );
```

On Windows Vista and later, the parameters passed to the callback function include the following:




<table>
<tr>
<th>Parameter</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="IN_PVOID_ApcContext"></a><a id="in_pvoid_apccontext"></a><a id="IN_PVOID_APCCONTEXT"></a>IN PVOID ApcContext

</td>
<td width="60%">
The <i>ApcContext</i> parameter passed to the <b>Icmp6SendEcho2</b> function. This parameter can be used by the application to identify the <b>Icmp6SendEcho2</b> request that the callback function is responding to. 

</td>
</tr>
<tr>
<td width="40%">
<a id="IN_PIO_STATUS_BLOCK_IoStatusBlock"></a><a id="in_pio_status_block_iostatusblock"></a><a id="IN_PIO_STATUS_BLOCK_IOSTATUSBLOCK"></a>IN PIO_STATUS_BLOCK IoStatusBlock

</td>
<td width="60%">
A pointer to a <b>IO_STATUS_BLOCK</b>. This variable contains the final completion status and information about the operation.  The number of bytes actually received in the reply is returned in the <b>Information</b> member of the <b>IO_STATUS_BLOCK</b> struct.

The <b>IO_STATUS_BLOCK</b> structure is defined in the <i>Wdm.h</i> header file.

</td>
</tr>
<tr>
<td width="40%">
<a id="IN_ULONG_Reserved"></a><a id="in_ulong_reserved"></a><a id="IN_ULONG_RESERVED"></a>IN ULONG Reserved

</td>
<td width="60%">
This parameter is reserved. 

</td>
</tr>
</table>
 



On Windows Server 2003 and Windows XP, any application that calls the <b>Icmp6SendEcho2</b> function asynchronously using the <i>ApcRoutine</i> parameter must not define <b>PIO_APC_ROUTINE_DEFINED</b> to force the datatype for the <i>ApcRoutine</i> parameter to <b>FARPROC</b> rather than <b>PIO_APC_ROUTINE</b>. 

On Windows Server 2003 and Windows XP, the callback function pointed to by the <i>ApcRoutine</i> must be defined as a function of type <b>VOID</b> with the following syntax:


``` syntax
typedef
VOID WINAPI
(*FARPROC) (
    IN PVOID ApcContext,
    );
```

On Windows Server 2003 and Windows XP, the parameters passed to the callback function include the following:




<table>
<tr>
<th>Parameter</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="IN_PVOID_ApcContext"></a><a id="in_pvoid_apccontext"></a><a id="IN_PVOID_APCCONTEXT"></a>IN PVOID ApcContext

</td>
<td width="60%">
The <i>ApcContext</i> parameter passed to the <b>Icmp6SendEcho2</b> function. This parameter can be used by the application to identify the <b>Icmp6SendEcho2</b> request that the callback function is responding to. 

</td>
</tr>
</table>
 



The callback function specified in the <i>ApcRoutine</i> parameter must be implemented in the same process as the application calling the <b>Icmp6SendEcho2</b> function. If the callback function is in a separate DLL, then the DLL should be loaded before calling the <b>Icmp6SendEcho2</b> function. 

For IPv4, use the <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpcreatefile">IcmpCreateFile</a>,  <b>IcmpSendEcho</b>, <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2">IcmpSendEcho2</a>, <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2ex">IcmpSendEcho2Ex</a>, and <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpparsereplies">IcmpParseReplies</a> functions.

Note that the include directive for <i>Iphlpapi.h</i> header file must be placed before the <i>Icmpapi.h</i> header file.

## -see-also

<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventexa">CreateEventEx</a>



<a href="/windows/desktop/Sync/event-objects">Event Objects</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>



<a href="/windows/desktop/api/ipexport/ns-ipexport-icmpv6_echo_reply_lh">ICMPV6_ECHO_REPLY</a>



<a href="/windows/desktop/api/ipexport/ns-ipexport-icmp_echo_reply">ICMP_ECHO_REPLY</a>



<a href="/windows/desktop/api/ipexport/ns-ipexport-ip_option_information">IP_OPTION_INFORMATION</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6createfile">Icmp6CreateFile</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6parsereplies">Icmp6ParseReplies</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpclosehandle">IcmpCloseHandle</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpcreatefile">IcmpCreateFile</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpparsereplies">IcmpParseReplies</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho">IcmpSendEcho</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2">IcmpSendEcho2</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2ex">IcmpSendEcho2Ex</a>



<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a>
