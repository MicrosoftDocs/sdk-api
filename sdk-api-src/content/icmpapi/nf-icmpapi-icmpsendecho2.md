---
UID: NF:icmpapi.IcmpSendEcho2
title: IcmpSendEcho2 function (icmpapi.h)
description: The IcmpSendEcho2 function sends an IPv4 ICMP echo request and returns either immediately (if Event or ApcRoutine is non-NULL) or returns after the specified time-out. The ReplyBuffer contains the ICMP echo responses, if any.
helpviewer_keywords: ["IcmpSendEcho2","IcmpSendEcho2 function [IP Helper]","_iphlp_icmpsendecho2","icmpapi/IcmpSendEcho2","iphlp.icmpsendecho2"]
old-location: iphlp\icmpsendecho2.htm
tech.root: IpHlp
ms.assetid: 1f70b6cc-9085-4eb8-b2cc-3b3d98d0ea46
ms.date: 12/05/2018
ms.keywords: IcmpSendEcho2, IcmpSendEcho2 function [IP Helper], _iphlp_icmpsendecho2, icmpapi/IcmpSendEcho2, iphlp.icmpsendecho2
req.header: icmpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.dll: Iphlpapi.dll on Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP; Icmp.dll on Windows 2000 Server and Windows 2000 Professional
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IcmpSendEcho2
 - icmpapi/IcmpSendEcho2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
 - Icmp.dll
api_name:
 - IcmpSendEcho2
---

# IcmpSendEcho2 function


## -description

The 
<b>IcmpSendEcho2</b> function sends an IPv4 ICMP echo request and returns either immediately (if <i>Event</i> or <i>ApcRoutine</i> is non-<b>NULL</b>) or returns after the specified time-out. The <i>ReplyBuffer</i> contains the ICMP echo responses, if any.

## -parameters

### -param IcmpHandle [in]

The open handle returned by the <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpcreatefile">ICMPCreateFile</a> function.

### -param Event [in, optional]

An event to be signaled whenever an ICMP response arrives. If this parameter is specified, it requires a handle to a valid event object. Use the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> or <a href="/windows/desktop/api/synchapi/nf-synchapi-createeventexa">CreateEventEx</a> function to create this event object. 

For more information on using events, see <a href="/windows/desktop/Sync/event-objects">Event Objects</a>.

### -param ApcRoutine [in, optional]

The routine that is called when the calling thread is in an alertable thread and  an ICMPv4 reply arrives. On Windows Vista and later, <b>PIO_APC_ROUTINE_DEFINED</b> must be defined to force the datatype for this parameter to <b>PIO_APC_ROUTINE</b> rather than <b>FARPROC</b>. 

On Windows Server 2003, Windows XP, and Windows 2000, 
   <b>PIO_APC_ROUTINE_DEFINED</b> must not be defined to force the datatype for this parameter to <b>FARPROC</b>.

### -param ApcContext [in, optional]

An optional parameter passed to the callback routine specified in the  <i>ApcRoutine</i> parameter whenever an ICMP response arrives or an error occurs.

### -param DestinationAddress [in]

The IPv4 destination of the echo request, in the form of an <a href="/windows/desktop/api/inaddr/ns-inaddr-in_addr">IPAddr</a> structure.

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

When called synchronously, the <b>IcmpSendEcho2</b> function returns the number of replies received and stored in <i>ReplyBuffer</i>. If the return value is zero, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> for extended error information.

When called asynchronously, the <b>IcmpSendEcho2</b> function returns ERROR_IO_PENDING to indicate the operation is in progress. The results can be retrieved later when the event specified in the <i>Event</i> parameter signals or the callback function in the <i>ApcRoutine</i> parameter is called.

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
The operation is in progress. This value is returned by a successful asynchronous call to <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2">IcmpSendEcho2</a> and is not an indication of an error.  

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

The <b>IcmpSendEcho2</b> function is called synchronously if the <i>ApcRoutine</i> or <i>Event</i> parameters are <b>NULL</b>. When called synchronously, the return value contains the number of replies received and stored in <i>ReplyBuffer</i> after waiting for the time specified in the <i>Timeout</i> parameter. If the return value is zero, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> for extended error information.

The <b>IcmpSendEcho2</b> function is called asynchronously when either the <i>ApcRoutine</i> or <i>Event</i> parameters are specified. When called asynchronously,  the <i>ReplyBuffer</i> and <i>ReplySize</i> parameters are  required to accept the response. ICMP response data is copied to the <i>ReplyBuffer</i> provided and the application is signaled (when the <i>Event</i> parameter is specified) or the callback function is called (when the <i>ApcRoutine</i> parameter is specified). The application must parse the data pointed to by <i>ReplyBuffer</i> parameter using the <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpparsereplies">IcmpParseReplies</a> function. 

If the <i>Event</i> parameter is specified, the <b>IcmpSendEcho2</b> function is called asynchronously. The event specified in the <i>Event</i> parameter is signaled whenever an ICMP response arrives. Use the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> function to create this event object. 

If the <i>ApcRoutine</i> parameter is specified, the <b>IcmpSendEcho2</b> function is called asynchronously. The <i>ApcRoutine</i>  parameter should point to a user-defined callback function. The callback function specified in the <i>ApcRoutine</i> parameter is called whenever an ICMP response arrives. The invocation of the callback function specified in the <i>ApcRoutine</i> parameter is serialized. 

If both the <i>Event</i> and <i>ApcRoutine</i> parameters are specified, the event specified in the <i>Event</i> parameter is signaled whenever an ICMP response arrives, but the callback function specified in the <i>ApcRoutine</i> parameter is ignored . 

On Windows Vista and later, any application that calls <b>IcmpSendEcho2</b> function asynchronously using the <i>ApcRoutine</i> parameter must define <b>PIO_APC_ROUTINE_DEFINED</b> to force the datatype for the <i>ApcRoutine</i> parameter to <b>PIO_APC_ROUTINE</b> rather than <b>FARPROC</b>. <div class="alert"><b>Note</b>  <b>PIO_APC_ROUTINE_DEFINED</b> must be defined before the <i>Icmpapi.h</i> header file is included.</div>
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
The <i>ApcContext</i> parameter passed to the <b>IcmpSendEcho2</b> function. This parameter can be used by the application to identify the <b>IcmpSendEcho2</b> request that the callback function is responding to. 

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
 



On Windows Server 2003, Windows XP, and  Windows 2000, any application that calls the <b>IcmpSendEcho2</b> function asynchronously using the <i>ApcRoutine</i> parameter must not define <b>PIO_APC_ROUTINE_DEFINED</b> to force the datatype for the <i>ApcRoutine</i> parameter to <b>FARPROC</b> rather than <b>PIO_APC_ROUTINE</b>. 

On Windows Server 2003 and Windows XP, the callback function pointed to by the <i>ApcRoutine</i> must be defined as a function of type <b>VOID</b> with the following syntax:


``` syntax
typedef
VOID WINAPI
(*FARPROC) (
    IN PVOID ApcContext,
    );
```

On Windows Server 2003, Windows XP, and Windows 2000, the parameters passed to the callback function include the following:




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
The <i>ApcContext</i> parameter passed to the <b>IcmpSendEcho2</b> function. This parameter can be used by the application to identify the <b>IcmpSendEcho2</b> request that the callback function is responding to. 

</td>
</tr>
</table>
 



The callback function specified in the <i>ApcRoutine</i> parameter must be implemented in the same process as the application calling the <b>IcmpSendEcho2</b> function. If the callback function is in a separate DLL, then the DLL should be loaded before calling the <b>IcmpSendEcho2</b> function. 

The <b>IcmpSendEcho2</b> function is exported from the <i>Icmp.dll</i> on Windows 2000. The <b>IcmpSendEcho2</b> function is exported from the <i>Iphlpapi.dll</i> on Windows XP and later. Windows version checking is not recommended to use this function. Applications requiring portability  with this function across Windows 2000, Windows XP, Windows Server 2003 and later Windows versions should not statically link to either the <i>Icmp.lib</i> or the <i>Iphlpapi.lib</i> file. Instead, the application should check for the presence of <b>IcmpSendEcho2</b> in the <i>Iphlpapi.dll</i> with calls to <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>.  Failing that, the application should check for the presence of <b>IcmpSendEcho2</b> in the <i>Icmp.dll</i> with  calls to <b>LoadLibrary</b> and <b>GetProcAddress</b>. 

For IPv6, use the <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6createfile">Icmp6CreateFile</a>, <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6sendecho2">Icmp6SendEcho2</a>, and <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6parsereplies">Icmp6ParseReplies</a> functions.

Note that the include directive for <i>Iphlpapi.h</i> header file must be placed before the <i>Icmpapi.h</i> header file.


#### Examples

The following example calls the <b>IcmpSendEcho2</b> function synchronously. The example sends an ICMP echo request to the IP address specified on the command line and prints the information received from the first response.


```cpp
#include <winsock2.h>
#include <iphlpapi.h>
#include <icmpapi.h>
#include <stdio.h>

#pragma comment(lib, "iphlpapi.lib")
#pragma comment(lib, "ws2_32.lib")

int __cdecl main(int argc, char **argv)
{

    // Declare and initialize variables

    HANDLE hIcmpFile;
    unsigned long ipaddr = INADDR_NONE;
    DWORD dwRetVal = 0;
    DWORD dwError = 0;
    char SendData[] = "Data Buffer";
    LPVOID ReplyBuffer = NULL;
    DWORD ReplySize = 0;

    // Validate the parameters
    if (argc != 2) {
        printf("usage: %s IP address\n", argv[0]);
        return 1;
    }

    ipaddr = inet_addr(argv[1]);
    if (ipaddr == INADDR_NONE) {
        printf("usage: %s IP address\n", argv[0]);
        return 1;
    }

    hIcmpFile = IcmpCreateFile();
    if (hIcmpFile == INVALID_HANDLE_VALUE) {
        printf("\tUnable to open handle.\n");
        printf("IcmpCreatefile returned error: %ld\n", GetLastError());
        return 1;
    }
    // Allocate space for at a single reply
    ReplySize = sizeof (ICMP_ECHO_REPLY) + sizeof (SendData) + 8;
    ReplyBuffer = (VOID *) malloc(ReplySize);
    if (ReplyBuffer == NULL) {
        printf("\tUnable to allocate memory for reply buffer\n");
        return 1;
    }

    dwRetVal = IcmpSendEcho2(hIcmpFile, NULL, NULL, NULL,
                             ipaddr, SendData, sizeof (SendData), NULL,
                             ReplyBuffer, ReplySize, 1000);
    if (dwRetVal != 0) {
        PICMP_ECHO_REPLY pEchoReply = (PICMP_ECHO_REPLY) ReplyBuffer;
        struct in_addr ReplyAddr;
        ReplyAddr.S_un.S_addr = pEchoReply->Address;
        printf("\tSent icmp message to %s\n", argv[1]);
        if (dwRetVal > 1) {
            printf("\tReceived %ld icmp message responses\n", dwRetVal);
            printf("\tInformation from the first response:\n");
        } else {
            printf("\tReceived %ld icmp message response\n", dwRetVal);
            printf("\tInformation from this response:\n");
        }
        printf("\t  Received from %s\n", inet_ntoa(ReplyAddr));
        printf("\t  Status = %ld  ", pEchoReply->Status);
        switch (pEchoReply->Status) {
        case IP_DEST_HOST_UNREACHABLE:
            printf("(Destination host was unreachable)\n");
            break;
        case IP_DEST_NET_UNREACHABLE:
            printf("(Destination Network was unreachable)\n");
            break;
        case IP_REQ_TIMED_OUT:
            printf("(Request timed out)\n");
            break;
        default:
            printf("\n");
            break;
        }

        printf("\t  Roundtrip time = %ld milliseconds\n",
               pEchoReply->RoundTripTime);
    } else {
        printf("Call to IcmpSendEcho2 failed.\n");
        dwError = GetLastError();
        switch (dwError) {
        case IP_BUF_TOO_SMALL:
            printf("\tReplyBufferSize too small\n");
            break;
        case IP_REQ_TIMED_OUT:
            printf("\tRequest timed out\n");
            break;
        default:
            printf("\tExtended error returned: %ld\n", dwError);
            break;
        }
        return 1;
    }
    return 0;
}

```

## -see-also

<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventexa">CreateEventEx</a>



<a href="/windows/desktop/Sync/event-objects">Event Objects</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>



<a href="/windows/desktop/api/ipexport/ns-ipexport-icmp_echo_reply">ICMP_ECHO_REPLY</a>



<a href="/windows/desktop/api/inaddr/ns-inaddr-in_addr">IPAddr</a>



<a href="/windows/desktop/api/ipexport/ns-ipexport-ip_option_information">IP_OPTION_INFORMATION</a>



<a href="/windows/desktop/api/ipexport/ns-ipexport-ip_option_information32">IP_OPTION_INFORMATION32</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6createfile">Icmp6CreateFile</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6parsereplies">Icmp6ParseReplies</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6sendecho2">Icmp6SendEcho2</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpclosehandle">IcmpCloseHandle</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpcreatefile">IcmpCreateFile</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpparsereplies">IcmpParseReplies</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho">IcmpSendEcho</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2ex">IcmpSendEcho2Ex</a>
