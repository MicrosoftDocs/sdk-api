---
UID: NF:icmpapi.Icmp6SendEcho2
title: Icmp6SendEcho2 function
author: windows-driver-content
description: The Icmp6SendEcho2 function sends an IPv6 ICMPv6 echo request and returns either immediately (if Event or ApcRoutine is non-NULL) or returns after the specified time-out. The ReplyBuffer contains the IPv6 ICMPv6 echo response, if any.
old-location: iphlp\icmp6sendecho2.htm
old-project: IpHlp
ms.assetid: 622c769b-ede8-4bc2-ac54-98de47ae1fed
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: Icmp6SendEcho2, Icmp6SendEcho2 function [IP Helper], icmpapi/Icmp6SendEcho2, iphlp.icmp6sendecho2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: icmpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NET_FW_SERVICE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Iphlpapi.dll
api_name:
-	Icmp6SendEcho2
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# Icmp6SendEcho2 function


## -description


The <b>Icmp6SendEcho2</b> function sends an IPv6 ICMPv6 echo request and returns either immediately (if <i>Event</i> or <i>ApcRoutine</i> is non-<b>NULL</b>) or returns after the specified time-out. The <i>ReplyBuffer</i> contains the IPv6 ICMPv6 echo response, if any.


## -parameters




### -param IcmpHandle [in]

The open handle returned by <a href="https://msdn.microsoft.com/2ddb23d8-a4e6-47c4-a552-2815ccaf055f">Icmp6CreateFile</a>.


### -param Event [in, optional]

An event to be signaled whenever an ICMPv6 response arrives. If this parameter is specified, it requires a handle to a valid event object. Use the 
<a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a> or <a href="https://msdn.microsoft.com/402a721d-8338-4df1-ba0b-074f868a1731">CreateEventEx</a> function to create this event object. 

For more information on using events, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff544323">Event Objects</a>.


### -param ApcRoutine [in, optional]

The routine that is called when the calling thread is in an alertable thread and  an ICMPv6 reply arrives. On Windows Vista and later, <b>PIO_APC_ROUTINE_DEFINED</b> must be defined to force the datatype for this parameter to <b>PIO_APC_ROUTINE</b> rather than <b>FARPROC</b>. 

On Windows Server 2003 and Windows XP
  , 
   <b>PIO_APC_ROUTINE_DEFINED</b> must not be defined to force the datatype for this parameter to <b>FARPROC</b>.


### -param ApcContext [in, optional]

An optional parameter passed to the callback routine specified in the  <i>ApcRoutine</i> parameter whenever an ICMPv6 response arrives or an error occurs. 


### -param SourceAddress [in]

The IPv6 source address on which to issue the echo request, in the form of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">sockaddr</a> structure.


### -param DestinationAddress [in]

The IPv6 destination address of the echo request, in the form of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">sockaddr</a> structure.


### -param RequestData [in]

A pointer to a buffer that contains data to send in the request.


### -param RequestSize [in]

The size, in bytes, of the request data buffer pointed to by the <i>RequestData</i> parameter.


### -param RequestOptions [in, optional]

A pointer to the IPv6 header options for the request, in the form of an <a href="https://msdn.microsoft.com/4341d0a4-65d8-4677-b208-2cde5ff36f14">IP_OPTION_INFORMATION</a> structure. On a 64-bit platform, this parameter is in the form for an <a href="https://msdn.microsoft.com/3924230d-ff10-43ac-981c-81273bce6896">IP_OPTION_INFORMATION32</a> structure.

This parameter may be NULL if no IP header options need to be specified.

<div class="alert"><b>Note</b>  On Windows Server 2003 and Windows XP, the <i>RequestOptions</i> parameter is not optional and must not be NULL and only the <b>Ttl</b> and <b>Flags</b> members are used.</div>
<div> </div>

### -param ReplyBuffer [out]

A pointer to a buffer to hold replies to the request. Upon return, the buffer contains an <a href="https://msdn.microsoft.com/8ea4ce42-6164-4b8e-9e79-524f456c8d09">ICMPV6_ECHO_REPLY</a> structure followed by the message body from the ICMPv6 echo response reply data. The buffer must be large enough to hold at least one 
<b>ICMPV6_ECHO_REPLY</b> structure plus the number of bytes of data specified in the <i>RequestSize</i> parameter. This buffer should also be large enough to also hold 8 more bytes of data (the size of an ICMP error message) plus space for an <b>IO_STATUS_BLOCK</b> structure.



### -param ReplySize [in]

The size, in bytes,  of the reply buffer pointed to by the <i>ReplyBuffer</i> parameter. This buffer should be large enough to hold at least one 
<a href="https://msdn.microsoft.com/8ea4ce42-6164-4b8e-9e79-524f456c8d09">ICMPV6_ECHO_REPLY</a> structure plus <i>RequestSize</i> bytes of data. This buffer should also be large enough to also hold 8 more bytes of data (the size of an ICMP error message) plus space for an <b>IO_STATUS_BLOCK</b> structure.



### -param Timeout [in]

The time, in milliseconds, to wait for replies. This parameter is only used if the <b>Icmp6SendEcho2</b> function is called synchronously. So this parameter is not used if either the <i>ApcRoutine</i> or <i>Event</i>
                           parameter are not <b>NULL</b>.


## -returns



When called synchronously, the <b>Icmp6SendEcho2</b> function returns the number of replies received and stored in <i>ReplyBuffer</i>. If the return value is zero, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> for extended error information.

When called asynchronously, the <b>Icmp6SendEcho2</b> function returns ERROR_IO_PENDING  to indicate the operation is in progress. The results can be retrieved later when the event specified in the <i>Event</i> parameter signals or the callback function in the <i>ApcRoutine</i> parameter is called.

If the return value is zero, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> for extended error information.

If the function fails, the extended error code returned by <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> can be one of the following values.

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
The operation is in progress. This value is returned by a successful asynchronous call to <a href="https://msdn.microsoft.com/622c769b-ede8-4bc2-ac54-98de47ae1fed">Icmp6SendEcho2</a> and is not an indication of an error.  

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
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>
 




## -remarks



The <b>Icmp6SendEcho2</b> function is called synchronously if the <i>ApcRoutine</i> or <i>Event</i> parameters are <b>NULL</b>. When called synchronously, the return value contains the number of replies received and stored in <i>ReplyBuffer</i> after waiting for the time specified in the <i>Timeout</i> parameter. If the return value is zero, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> for extended error information.

The <b>Icmp6SendEcho2</b> function is called asynchronously when either the <i>ApcRoutine</i> or <i>Event</i> parameters are specified. When called asynchronously,  the <i>ReplyBuffer</i> and <i>ReplySize</i> parameters are  required to accept the response. ICMP response data is copied to the <i>ReplyBuffer</i> provided and the application is signaled (when the <i>Event</i> parameter is specified) or the callback function is called (when the <i>ApcRoutine</i> parameter is specified). The application must parse the data pointed to by <i>ReplyBuffer</i> parameter using the <a href="https://msdn.microsoft.com/b4d63ffd-37ad-4901-b017-205fb15381e7">Icmp6ParseReplies</a> function. 

If the <i>Event</i> parameter is specified, the <b>Icmp6SendEcho2</b> function is called asynchronously. The event specified in the <i>Event</i> parameter is signaled whenever an ICMPv6 response arrives. Use the 
<a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a> function to create this event object. 

If the <i>ApcRoutine</i> parameter is specified, the <b>Icmp6SendEcho2</b> function is called asynchronously. The <i>ApcRoutine</i>  parameter should point to a user-defined callback function. The callback function specified in the <i>ApcRoutine</i> parameter is called whenever an ICMPv6 response arrives. The invocation of the callback function specified in the <i>ApcRoutine</i> parameter is serialized. 

If both the <i>Event</i> and <i>ApcRoutine</i> parameters are specified, the event specified in the <i>Event</i> parameter is signaled whenever an ICMPv6 response arrives, but the callback function specified in the <i>ApcRoutine</i> parameter is ignored . 

On Windows Vista and later, any application that calls <b>Icmp6SendEcho2</b> function asynchronously using the <i>ApcRoutine</i> parameter must define <b>PIO_APC_ROUTINE_DEFINED</b> to force the datatype for the <i>ApcRoutine</i> parameter to <b>PIO_APC_ROUTINE</b> rather than <b>FARPROC</b>. <div class="alert"><b>Note</b>  <b>PIO_APC_ROUTINE_DEFINED</b> must be defined before the <i>Icmpapi.h</i> header file is included.</div>
<div> </div>


On Windows Vista and later, the callback function pointed to by the <i>ApcRoutine</i> must be defined as a function of type <b>VOID</b> with the following syntax:

<pre class="syntax" xml:space="preserve"><code>typedef
VOID WINAPI
(*PIO_APC_ROUTINE) (
    IN PVOID ApcContext,
    IN PIO_STATUS_BLOCK IoStatusBlock,
    IN ULONG Reserved
    );</code></pre>
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
 



On Windows Server 2003 and Windows XP
  , any application that calls the <b>Icmp6SendEcho2</b> function asynchronously using the <i>ApcRoutine</i> parameter must not define <b>PIO_APC_ROUTINE_DEFINED</b> to force the datatype for the <i>ApcRoutine</i> parameter to <b>FARPROC</b> rather than <b>PIO_APC_ROUTINE</b>. 

On Windows Server 2003 and Windows XP, the callback function pointed to by the <i>ApcRoutine</i> must be defined as a function of type <b>VOID</b> with the following syntax:

<pre class="syntax" xml:space="preserve"><code>typedef
VOID WINAPI
(*FARPROC) (
    IN PVOID ApcContext,
    );</code></pre>
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

For IPv4, use the <a href="https://msdn.microsoft.com/b435b38b-df86-4991-9772-c712c9ea606f">IcmpCreateFile</a>,  <b>IcmpSendEcho</b>, <a href="https://msdn.microsoft.com/1f70b6cc-9085-4eb8-b2cc-3b3d98d0ea46">IcmpSendEcho2</a>, <a href="https://msdn.microsoft.com/7b2b2cae-650f-4ecb-aa2e-a55ee4026999">IcmpSendEcho2Ex</a>, and <a href="https://msdn.microsoft.com/ec7c2a5f-5406-4350-b795-6e72fe25f62d">IcmpParseReplies</a> functions.

Note that the include directive for <i>Iphlpapi.h</i> header file must be placed before the <i>Icmpapi.h</i> header file.




## -see-also




<a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a>



<a href="https://msdn.microsoft.com/402a721d-8338-4df1-ba0b-074f868a1731">CreateEventEx</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544323">Event Objects</a>



<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>



<a href="https://msdn.microsoft.com/8ea4ce42-6164-4b8e-9e79-524f456c8d09">ICMPV6_ECHO_REPLY</a>



<a href="https://msdn.microsoft.com/e6d43c35-1009-4df1-bc39-aec97178cae6">ICMP_ECHO_REPLY</a>



<a href="https://msdn.microsoft.com/4341d0a4-65d8-4677-b208-2cde5ff36f14">IP_OPTION_INFORMATION</a>



<a href="https://msdn.microsoft.com/2ddb23d8-a4e6-47c4-a552-2815ccaf055f">Icmp6CreateFile</a>



<a href="https://msdn.microsoft.com/b4d63ffd-37ad-4901-b017-205fb15381e7">Icmp6ParseReplies</a>



<a href="https://msdn.microsoft.com/ce8f11bb-1e33-41bd-adb9-c18efadd4d0b">IcmpCloseHandle</a>



<a href="https://msdn.microsoft.com/b435b38b-df86-4991-9772-c712c9ea606f">IcmpCreateFile</a>



<a href="https://msdn.microsoft.com/ec7c2a5f-5406-4350-b795-6e72fe25f62d">IcmpParseReplies</a>



<a href="https://msdn.microsoft.com/c3cdc535-2c13-48c6-9ab1-88cc5e5119b5">IcmpSendEcho</a>



<a href="https://msdn.microsoft.com/1f70b6cc-9085-4eb8-b2cc-3b3d98d0ea46">IcmpSendEcho2</a>



<a href="https://msdn.microsoft.com/7b2b2cae-650f-4ecb-aa2e-a55ee4026999">IcmpSendEcho2Ex</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">sockaddr</a>
 

 

