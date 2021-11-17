---
UID: NF:icmpapi.IcmpSendEcho2Ex
title: IcmpSendEcho2Ex function (icmpapi.h)
description: Sends an IPv4 ICMP echo request and returns either immediately (if Event or ApcRoutine is non-NULL) or returns after the specified time-out. The ReplyBuffer contains the ICMP responses, if any.
helpviewer_keywords: ["IcmpSendEcho2Ex","IcmpSendEcho2Ex function [IP Helper]","icmpapi/IcmpSendEcho2Ex","iphlp.icmpsendecho2ex"]
old-location: iphlp\icmpsendecho2ex.htm
tech.root: IpHlp
ms.assetid: 7b2b2cae-650f-4ecb-aa2e-a55ee4026999
ms.date: 12/05/2018
ms.keywords: IcmpSendEcho2Ex, IcmpSendEcho2Ex function [IP Helper], icmpapi/IcmpSendEcho2Ex, iphlp.icmpsendecho2ex
req.header: icmpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IcmpSendEcho2Ex
 - icmpapi/IcmpSendEcho2Ex
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
 - IcmpSendEcho2Ex
---

# IcmpSendEcho2Ex function


## -description

The 
<b>IcmpSendEcho2Ex</b> function sends an IPv4 ICMP echo request and returns either immediately (if <i>Event</i> or <i>ApcRoutine</i> is non-<b>NULL</b>) or returns after the specified time-out. The <i>ReplyBuffer</i> contains the ICMP responses, if any.

## -parameters

### -param IcmpHandle [in]

An open handle returned by the <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpcreatefile">ICMPCreateFile</a> function.

### -param Event [in, optional]

An event to be signaled whenever an ICMP response arrives. If this parameter is specified, it requires a handle to a valid event object. Use the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> or <a href="/windows/desktop/api/synchapi/nf-synchapi-createeventexa">CreateEventEx</a> function to create this event object. 

For more information on using events, see <a href="/windows/desktop/Sync/event-objects">Event Objects</a>.

### -param ApcRoutine [in, optional]

The routine that is called when the calling thread is in an alertable thread and  an ICMP reply arrives. <b>PIO_APC_ROUTINE_DEFINED</b> must be defined to force the datatype for this parameter to <b>PIO_APC_ROUTINE</b> rather than <b>FARPROC</b>.

### -param ApcContext [in, optional]

An optional parameter passed to the callback routine specified in the  <i>ApcRoutine</i> parameter whenever an ICMP response arrives or an error occurs.

### -param SourceAddress [in]

The IPv4 source address on which to issue the echo request. This address is in the form of an <a href="/windows/desktop/api/inaddr/ns-inaddr-in_addr">IPAddr</a> structure.

### -param DestinationAddress [in]

The IPv4 destination address for the echo request. This address is in the form of an <a href="/windows/desktop/api/inaddr/ns-inaddr-in_addr">IPAddr</a> structure.

### -param RequestData [in]

A pointer to a buffer that contains data to send in the request.

### -param RequestSize [in]

The size, in bytes, of the request data buffer pointed to by the <i>RequestData</i> parameter.

### -param RequestOptions [in, optional]

A pointer to the IP header options for the request, in the form of an <a href="/windows/desktop/api/ipexport/ns-ipexport-ip_option_information">IP_OPTION_INFORMATION</a> structure. On a 64-bit platform, this parameter is in the form for an <a href="/windows/desktop/api/ipexport/ns-ipexport-ip_option_information32">IP_OPTION_INFORMATION32</a> structure.

This parameter may be <b>NULL</b> if no IP header options need to be specified.

### -param ReplyBuffer [out]

A pointer to a buffer to hold any replies to the request. Upon return, the buffer contains an array of 
<a href="/windows/desktop/api/ipexport/ns-ipexport-icmp_echo_reply">ICMP_ECHO_REPLY</a> structures followed by options and data. The buffer must be large enough to hold at least one 
<b>ICMP_ECHO_REPLY</b> structure plus <i>RequestSize</i> bytes of data.

This buffer should also be large enough to also hold 8 more bytes of data (the size of an ICMP error message) plus space for an <b>IO_STATUS_BLOCK</b> structure.

### -param ReplySize [in]

The allocated size, in bytes,  of the reply buffer. The buffer should be large enough to hold at least one 
<a href="/windows/desktop/api/ipexport/ns-ipexport-icmp_echo_reply">ICMP_ECHO_REPLY</a> structure plus <i>RequestSize</i> bytes of data.

This buffer should also be large enough to also hold 8 more bytes of data (the size of an ICMP error message) plus space for an <b>IO_STATUS_BLOCK</b> structure.

### -param Timeout [in]

The time, in milliseconds, to wait for replies.

## -returns

When called synchronously, the <b>IcmpSendEcho2Ex</b> function returns the number of replies received and stored in <i>ReplyBuffer</i>. If the return value is zero, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> for extended error information.

When called asynchronously, the <b>IcmpSendEcho2Ex</b> function returns ERROR_IO_PENDING  to indicate the operation is in progress. The results can be retrieved later when the event specified in the <i>Event</i> parameter signals or the callback function in the <i>ApcRoutine</i> parameter is called.

If the return value is zero, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> for extended error information.

If the function fails, the extended error code returned by <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> can be one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if the <i>IcmpHandle</i> parameter contains an invalid handle. This error can also be returned if the <i>ReplySize</i> parameter specifies a value less than the size of an <a href="/windows/desktop/api/ipexport/ns-ipexport-icmp_echo_reply">ICMP_ECHO_REPLY</a> structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_IO_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The operation is in progress. This value is returned by a successful asynchronous call to <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2ex">IcmpSendEcho2Ex</a> and is not an indication of an error.  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory is available to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if no IPv4 stack is on the local computer.

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

The <b>IcmpSendEcho2Ex</b> function is available on Windows Server 2008 and later. 

The <b>IcmpSendEcho2Ex</b> function is an enhanced version of the <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2">IcmpSendEcho2</a> function that allows the user to specify the IPv4 source address on which to issue the ICMP request. The <b>IcmpSendEcho2Ex</b> function is useful in cases where a computer has multiple network interfaces.

The <b>IcmpSendEcho2Ex</b> function is called synchronously if the <i>ApcRoutine</i> or <i>Event</i> parameters are <b>NULL</b>. When called synchronously, the return value contains the number of replies received and stored in <i>ReplyBuffer</i> after waiting for the time specified in the <i>Timeout</i> parameter. If the return value is zero, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> for extended error information.

The <b>IcmpSendEcho2Ex</b> function is called asynchronously when either the <i>ApcRoutine</i> or <i>Event</i> parameters are specified. When called asynchronously,  the <i>ReplyBuffer</i> and <i>ReplySize</i> parameters are  required to accept the response. ICMP response data is copied to the <i>ReplyBuffer</i> provided and the application is signaled (when the <i>Event</i> parameter is specified) or the callback function is called (when the <i>ApcRoutine</i> parameter is specified). The application must parse the data pointed to by <i>ReplyBuffer</i> parameter using the <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpparsereplies">IcmpParseReplies</a> function. 

If the <i>Event</i> parameter is specified, the <b>IcmpSendEcho2Ex</b> function is called asynchronously. The event specified in the <i>Event</i> parameter is signaled whenever an ICMP response arrives. Use the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> function to create this event object. 

If the <i>ApcRoutine</i> parameter is specified, the <b>IcmpSendEcho2Ex</b> function is called asynchronously. The <i>ApcRoutine</i>  parameter should point to a user-defined callback function. The callback function specified in the <i>ApcRoutine</i> parameter is called whenever an ICMP response arrives. The invocation of the callback function specified in the <i>ApcRoutine</i> parameter is serialized. 

If both the <i>Event</i> and <i>ApcRoutine</i> parameters are specified, the event specified in the <i>Event</i> parameter is signaled whenever an ICMP response arrives, but the callback function specified in the <i>ApcRoutine</i> parameter is ignored . 

Any application that calls the <b>IcmpSendEcho2Ex</b> function asynchronously using the <i>ApcRoutine</i> parameter must define <b>PIO_APC_ROUTINE_DEFINED</b> to force the datatype for the <i>ApcRoutine</i> parameter to <b>PIO_APC_ROUTINE</b> rather than <b>FARPROC</b>. <div class="alert"><b>Note</b>  <b>PIO_APC_ROUTINE_DEFINED</b> must be defined before the <i>Icmpapi.h</i> header file is included.</div>
<div> </div>


The callback function pointed to by the <i>ApcRoutine</i> must be defined as a function of type <b>VOID</b> with the following syntax:


``` syntax
typedef
VOID WINAPI
(*PIO_APC_ROUTINE) (
    IN PVOID ApcContext,
    IN PIO_STATUS_BLOCK IoStatusBlock,
    IN ULONG Reserved
    );
```

The parameters passed to the callback function include the following:




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
The <i>ApcContext</i> parameter passed to the <b>IcmpSendEcho2Ex</b> function. This parameter can be used by the application to identify the <b>IcmpSendEcho2Ex</b> request that the callback function is responding to. 

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
 



The callback function specified in the <i>ApcRoutine</i> parameter must be implemented in the same process as the application calling the <b>IcmpSendEcho2Ex</b> function. If the callback function is in a separate DLL, then the DLL should be loaded before calling the <b>IcmpSendEcho2Ex</b> function. 

For IPv6, use the <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6createfile">Icmp6CreateFile</a>, <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6sendecho2">Icmp6SendEcho2</a>, and <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6parsereplies">Icmp6ParseReplies</a> functions.

Note that the include directive for <i>Iphlpapi.h</i> header file must be placed before the <i>Icmpapi.h</i> header file.

## -see-also

<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventexa">CreateEventEx</a>



<a href="/windows/desktop/Sync/event-objects">Event Objects</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpcreatefile">ICMPCreateFile</a>



<a href="/windows/desktop/api/ipexport/ns-ipexport-icmp_echo_reply">ICMP_ECHO_REPLY</a>



<a href="/windows/desktop/api/inaddr/ns-inaddr-in_addr">IPAddr</a>



<a href="/windows/desktop/api/ipexport/ns-ipexport-ip_option_information">IP_OPTION_INFORMATION</a>



<a href="/windows/desktop/api/ipexport/ns-ipexport-ip_option_information32">IP_OPTION_INFORMATION32</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6createfile">Icmp6CreateFile</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6parsereplies">Icmp6ParseReplies</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6sendecho2">Icmp6SendEcho2</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpparsereplies">IcmpParseReplies</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho">IcmpSendEcho</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2">IcmpSendEcho2</a>
