---
UID: NF:icmpapi.IcmpSendEcho2
title: IcmpSendEcho2 function (icmpapi.h)
description: The **IcmpSendEcho2** function sends an IPv4 ICMP echo request, and returns either immediately (if *Event* or *ApcRoutine* is non-**NULL**), or returns after the specified time-out. The *ReplyBuffer* contains the ICMP echo responses, if any.
helpviewer_keywords: ["IcmpSendEcho2","IcmpSendEcho2 function [IP Helper]","_iphlp_icmpsendecho2","icmpapi/IcmpSendEcho2","iphlp.icmpsendecho2"]
old-location: iphlp\icmpsendecho2.htm
tech.root: IpHlp
ms.assetid: 1f70b6cc-9085-4eb8-b2cc-3b3d98d0ea46
ms.date: 03/24/2023
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

## -description

The **IcmpSendEcho2** function sends an IPv4 ICMP echo request, and returns either immediately (if *Event* or *ApcRoutine* is non-**NULL**), or returns after the specified time-out. The *ReplyBuffer* contains the ICMP echo responses, if any.

## -parameters

### -param IcmpHandle [in]

The open handle returned by the [ICMPCreateFile](/windows/win32/api/icmpapi/nf-icmpapi-icmpcreatefile) function.

### -param Event [in, optional]

An event to be signaled (at most once) when an ICMP response arrives. If this parameter is specified, then it requires a handle to a valid event object. Use the [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) or [CreateEventEx](/windows/win32/api/synchapi/nf-synchapi-createeventexa) function to create this event object.

For more information on using events, see [Event objects](/windows/win32/Sync/event-objects).

### -param ApcRoutine [in, optional]

The routine that's called when the calling thread is in an alertable thread, and an ICMPv4 reply arrives. **PIO_APC_ROUTINE_DEFINED** must be defined in order to force the datatype for this parameter to **PIO_APC_ROUTINE** rather than **FARPROC**.

### -param ApcContext [in, optional]

An optional parameter passed to the callback routine specified in the *ApcRoutine* parameter (at most once) when an ICMP response arrives, or an error occurs.

### -param DestinationAddress [in]

The IPv4 destination of the echo request, in the form of an [IPAddr](/windows/win32/api/inaddr/ns-inaddr-in_addr) structure.

### -param RequestData [in]

A pointer to a buffer that contains data to send in the request.

### -param RequestSize [in]

The size, in bytes, of the request data buffer pointed to by the *RequestData* parameter.

### -param RequestOptions [in, optional]

A pointer to the IP header options for the request, in the form of an [IP_OPTION_INFORMATION](/windows/win32/api/ipexport/ns-ipexport-ip_option_information) structure.

This parameter may be **NULL** if no IP header options need to be specified.

### -param ReplyBuffer [out]

A pointer to a buffer to hold any replies to the request. Upon return, the buffer contains an array of [ICMP_ECHO_REPLY](/windows/win32/api/ipexport/ns-ipexport-icmp_echo_reply) structures followed by options and data.

The buffer must be large enough to hold at least one **ICMP_ECHO_REPLY** structure, plus *RequestSize* bytes of data, plus an additional 8 bytes of data (the size of an ICMP error message).

### -param ReplySize [in]

The allocated size, in bytes, of the reply buffer.

The buffer must be large enough to hold at least one **ICMP_ECHO_REPLY** structure, plus *RequestSize* bytes of data, plus an additional 8 bytes of data (the size of an ICMP error message).

### -param Timeout [in]

The time in milliseconds to wait for replies.

## -returns

When called synchronously, the **IcmpSendEcho2** function returns the number of replies received and stored in *ReplyBuffer*. If the return value is zero, then for extended error information call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

When called asynchronously, the **IcmpSendEcho2** function returns zero. A subsequent call to [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns extended error code **ERROR_IO_PENDING** to indicate that the operation is in progress. The results can be retrieved later when the event specified in the *Event* parameter signals, or the callback function in the *ApcRoutine* parameter is called.

If the return value is zero, then for extended error information call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

If the function fails, then the extended error code returned by **GetLastError** can be one of the following values.

|Return code|Description|
|-|-|
|**ERROR_INVALID_PARAMETER**|An invalid parameter was passed to the function. This error is returned if the *IcmpHandle* parameter contains an invalid handle. This error can also be returned if the *ReplySize* parameter specifies a value less than the size of an [ICMP_ECHO_REPLY](/windows/win32/api/ipexport/ns-ipexport-icmp_echo_reply) structure.|
|**ERROR_IO_PENDING**|The operation is in progress. This value is returned by a successful asynchronous call to **IcmpSendEcho2**, and is not an indication of an error.|
|**ERROR_NOT_ENOUGH_MEMORY**|Not enough memory is available to complete the operation.|
|**ERROR_NOT_SUPPORTED**|The request is not supported. This error is returned if no IPv4 stack is on the local computer.|
|**IP_BUF_TOO_SMALL**|The size of the *ReplyBuffer* specified in the *ReplySize* parameter was too small.|
|**Other**|Use [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) to obtain the message string for the returned error.|

## -remarks

The **IcmpSendEcho2** function is called synchronously if the *ApcRoutine* or *Event* parameters are **NULL**. When called synchronously, the return value contains the number of replies received and stored in *ReplyBuffer* after waiting for the time specified in the *Timeout* parameter. If the return value is zero, then for extended error information call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

The **IcmpSendEcho2** function is called asynchronously when either the *ApcRoutine* or *Event* parameters are specified. When called asynchronously, the *ReplyBuffer* and *ReplySize* parameters are required to accept the response. ICMP response data is copied to the *ReplyBuffer* provided, and the application is signaled (when the *Event* parameter is specified) or the callback function is called (when the *ApcRoutine* parameter is specified). The application must parse the data pointed to by *ReplyBuffer* parameter using the [IcmpParseReplies](/windows/win32/api/icmpapi/nf-icmpapi-icmpparsereplies) function. 

If the *Event* parameter is specified, then the **IcmpSendEcho2** function is called asynchronously. The event specified in the *Event* parameter is signaled (at most once) when an ICMP response arrives. Use the [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) or [CreateEventEx](/windows/win32/api/synchapi/nf-synchapi-createeventexa) function to create this event object.

If the *ApcRoutine* parameter is specified, then the **IcmpSendEcho2** function is called asynchronously. The *ApcRoutine* parameter should point to a user-defined callback function. The callback function specified in the *ApcRoutine* parameter is called (at most once) when an ICMP response arrives. The invocation of the callback function specified in the *ApcRoutine* parameter is serialized.

If both the *Event* and *ApcRoutine* parameters are specified, then the event specified in the *Event* parameter is signaled (at most once) when an ICMP response arrives, but the callback function specified in the *ApcRoutine* parameter is ignored.

Any application that calls **IcmpSendEcho2** function asynchronously using the *ApcRoutine* parameter must define **PIO_APC_ROUTINE_DEFINED** to force the datatype for the *ApcRoutine* parameter to **PIO_APC_ROUTINE** rather than **FARPROC**.

> [!NOTE]
> **PIO_APC_ROUTINE_DEFINED** must be defined before the *Icmpapi.h* header file is included.

The callback function pointed to by the *ApcRoutine* must be defined as a function of type **VOID** with the following syntax:

```cpp
typedef
VOID WINAPI
(*PIO_APC_ROUTINE) (
    IN PVOID ApcContext,
    IN PIO_STATUS_BLOCK IoStatusBlock,
    IN ULONG Reserved
    );
```

The parameters passed to the callback function include the following:

|Parameter|Description|
|-|-|
|IN PVOID ApcContext|The *AppContext* parameter passed to the **IcmpSendEcho2** function. This parameter can be used by the application to identify the **IcmpSendEcho2** request that the callback function is responding to.|
|IN PIO_STATUS_BLOCK IoStatusBlock|A pointer to a **IO_STATUS_BLOCK**. This variable contains the final completion status and information about the operation. The number of bytes actually received in the reply is returned in the *Information* member of the **IO_STATUS_BLOCK** struct.<br/><br/>The **IO_STATUS_BLOCK** structure is defined in the `Wdm.h` header file.|
|IN ULONG Reserved|This parameter is reserved.|

The callback function specified in the *ApcRoutine* parameter must be implemented in the same process as the application calling the **IcmpSendEcho2** function. If the callback function is in a separate DLL, then the DLL should be loaded before calling the **IcmpSendEcho2** function. 

The **IcmpSendEcho2** function is exported from the `Iphlpapi.dll`.

For IPv6, use the [Icmp6CreateFile](/windows/win32/api/icmpapi/nf-icmpapi-icmp6createfile), [Icmp6SendEcho2](/windows/win32/api/icmpapi/nf-icmpapi-icmp6sendecho2), and [Icmp6ParseReplies](/windows/win32/api/icmpapi/nf-icmpapi-icmp6parsereplies) functions.

The include directive for the `Iphlpapi.h` header file must be placed before the one for the `Icmpapi.h` header file.

## Example

The following example calls the **IcmpSendEcho2** function synchronously. The example sends an ICMP echo request to the IP address specified on the command line, and prints the information received from the first response.

```cpp
#include <winsock2.h>
#include <iphlpapi.h>
#include <icmpapi.h>
#include <stdio.h>

#pragma comment(lib, "iphlpapi.lib")
#pragma comment(lib, "ws2_32.lib")

int __cdecl main(int argc, char **argv)
{
    // Declare and initialize variables.
    HANDLE hIcmpFile;
    unsigned long ipaddr = INADDR_NONE;
    DWORD dwRetVal = 0;
    DWORD dwError = 0;
    char SendData[] = "Data Buffer";
    LPVOID ReplyBuffer = NULL;
    DWORD ReplySize = 0;

    // Validate the parameters.
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

    // Allocate space for a single reply.
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

* [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa)
* [CreateEventEx](/windows/win32/api/synchapi/nf-synchapi-createeventexa)
* [Event objects](/windows/win32/Sync/event-objects)
* [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
* [ICMP_ECHO_REPLY](/windows/win32/api/ipexport/ns-ipexport-icmp_echo_reply)
* [IP_OPTION_INFORMATION](/windows/win32/api/ipexport/ns-ipexport-ip_option_information)
* [IP_OPTION_INFORMATION32](/windows/win32/api/ipexport/ns-ipexport-ip_option_information32)
* [IPAddr](/windows/win32/api/inaddr/ns-inaddr-in_addr)
* [Icmp6CreateFile](/windows/win32/api/icmpapi/nf-icmpapi-icmp6createfile)
* [Icmp6ParseReplies](/windows/win32/api/icmpapi/nf-icmpapi-icmp6parsereplies)
* [Icmp6SendEcho2](/windows/win32/api/icmpapi/nf-icmpapi-icmp6sendecho2)
* [IcmpCloseHandle](/windows/win32/api/icmpapi/nf-icmpapi-icmpclosehandle)
* [IcmpCreateFile](/windows/win32/api/icmpapi/nf-icmpapi-icmpcreatefile)
* [IcmpParseReplies](/windows/win32/api/icmpapi/nf-icmpapi-icmpparsereplies)
* [IcmpSendEcho](/windows/win32/api/icmpapi/nf-icmpapi-icmpsendecho)
* [IcmpSendEcho2Ex](/windows/win32/api/icmpapi/nf-icmpapi-icmpsendecho2ex)
