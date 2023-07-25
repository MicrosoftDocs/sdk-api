---
UID: NF:windns.DnsQueryRaw
title: DnsQueryRaw
description: Enables you to perform a DNS query that accepts either a raw packet containing a DNS query, or a query name and type.
tech.root: DNS
ms.date: 07/17/2023
targetos: Windows
prerelease: true
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: dnsapi.dll
req.header: windns.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: dnsapi.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: Windows
req.type-library: 
req.typenames: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dnsapi.dll
api_name:
 - DnsQueryRaw
f1_keywords:
 - DnsQueryRaw
 - windns/DnsQueryRaw
dev_langs:
 - c++
helpviewer_keywords:
 - DnsQueryRaw
---

## -description

Enables you to perform a DNS query that accepts either a raw packet containing a DNS query, or a query name and type. You can augment the query with settings and configuration from the host system.

* You can apply new query options and custom servers to an already-formatted raw DNS query packet.
* Or you can instead provide a query name and type, and receive both the parsed records and raw result packet (allowing clients to interact with all information received from the server).

Queries are performed asynchronously; and results are passed to a [DNS_QUERY_RAW_COMPLETION_ROUTINE](nc-windns-dns_query_raw_completion_routine.md) asynchronous callback function that you implement. To cancel a query, call [DnsCancelQueryRaw](./nf-windns-dnscancelqueryraw.md).

## -parameters

### -param queryRequest

Type: \_In\_ **[DNS_QUERY_RAW_REQUEST](./ns-windns-dns_query_raw_request.md)\***

The query request.

### -param cancelHandle

Type: \_Inout\_ **[DNS_QUERY_RAW_CANCEL](./ns-windns-dns_query_raw_cancel.md)\***

Used to obtain a cancel handle, which you can pass to [DnsCancelQueryRaw](./nf-windns-dnscancelqueryraw.md) should you need to cancel the query.

## -returns

A **DNS_STATUS** value indicating success or failure. If **DNS_REQUEST_PENDING** is returned, then when the query completes, the system calls the [DNS_QUERY_RAW_COMPLETION_ROUTINE](nc-windns-dns_query_raw_completion_routine.md) implementation that you passed in the *queryCompletionCallback* member of *queryRequest*. That callback will received the results of the query if successful, or any failures or cancellations.

## -remarks

The structure of a raw packet is the wire representation of the DNS query and response as documented by RFC 1035. A 12-byte DNS header is followed by either a question section for the query, or by a variable number (can be 0) of records for the response. If TCP is used, then the raw packet must be prefixed with a 2-byte *length* field. You can use this API to apply host NRPT rules, or to perform encrypted DNS queries, among other things.

## Examples

### Example 1

In this example, a raw query is read from a socket through a helper function, and the response is sent back through the same socket.

```cppwinrt
struct QUERY_RAW_CALLBACK_CONTEXT
{  
    DNS_QUERY_RAW_RESULT    *queryResults;
    HANDLE                  event;
};

VOID
CALLBACK
QueryRawCallback(
    _In_    VOID                  *queryContext,
    _In_    DNS_QUERY_RAW_RESULT  *queryResults
)
{
    QUERY_RAW_CALLBACK_CONTEXT *context = static_cast<QUERY_RAW_CALLBACK_CONTEXT *>(queryContext);

    //
    //  Capture the results of the query. Note that the DNS_QUERY_RAW_RESULT structure needs to
    //  be freed later with DnsQueryRawResultFree.
    //

    context->queryResults = queryResults;   

    SetEvent(context->event);
}

DWORD
HandleDnsQueryFromSocket(
    _In_ SOCKET socket
)
{
    DWORD errorStatus = ERROR_SUCCESS;
    DWORD waitStatus = 0;
    DNS_QUERY_RAW_REQUEST request = {0};
    DNS_QUERY_RAW_CANCEL cancel = {0};
    QUERY_RAW_CALLBACK_CONTEXT context = {0};
    CHAR opaqueSourceAddr[DNS_ADDR_MAX_SOCKADDR_LENGTH];
    ULONG opaqueSourceAddrSize = sizeof(opaqueSourceAddr);

    //
    //  ReceiveDnsQueryBytesFromSocket is a function that reads bytes from a socket
    //  that contains a wire-format DNS query, and gets information about the source
    //  address. It allocates the raw query buffer with HeapAlloc of size
    //  request.dnsQueryRawSize. Note that this function is just an example, and does
    //  not exist in the API.
    //
    errorStatus = ReceiveDnsQueryBytesFromSocket(socket,
                                                 &request.dnsQueryRaw,
                                                 &request.dnsQueryRawSize,
                                                 opaqueSourceAddr,
                                                 opaqueSourceAddrSize);
    if (errorStatus != ERROR_SUCCESS)
    {
        goto Exit;
    }

    context.event = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (context.event == NULL)
    {
        errorStatus = GetLastError();
        goto Exit;
    }

    //
    //  dnsQueryRaw is being used instead of dnsQueryName and dnsQueryType.
    //
    request.dnsQueryName = NULL;
    request.dnsQueryType = 0;

    request.version = DNS_QUERY_RAW_REQUEST_VERSION1; 
    request.resultsVersion = DNS_QUERY_RAW_RESULTS_VERSION1; 
    request.queryOptions = DNS_QUERY_BYPASS_CACHE;
    request.interfaceIndex = 0;
    request.queryCompletionCallback = &QueryRawCallback;
    request.queryContext = &context;
    request.queryRawOptions = 0;
    request.customServersSize = 0;
    request.customServers = NULL;
    request.protocol = DNS_PROTOCOL_UDP;
    memcpy_s(request.maxSa,
             sizeof(request.maxSa),
             opaqueSourceAddr,
             opaqueSourceAddrSize);

    errorStatus = DnsQueryRaw(&request, &cancel);
    if (errorStatus != DNS_REQUEST_PENDING)
    {
        goto Exit;
    }

    waitStatus = WaitForSingleObject(context.event, INFINITE);
    if (waitStatus != WAIT_OBJECT_0)
    {
        errorStatus = GetLastError();
        goto Exit;
    }

    //
    //  SendDnsResponseBytesToSocket is a function that writes a buffer containing a
    //  DNS response to a socket. Depending on the queryStatus, it can send other
    //  messages on the socket to indicate whether the socket should be closed, such as if
    //  the queryStatus indicates an internal DNS failure. Note that this function is
    //  just an example, and does not exist in the API.
    //
    errorStatus = SendDnsResponseBytesToSocket(socket,
                                               context.queryResults->queryStatus,
                                               context.queryResults->queryRawResponse,
                                               context.queryResults->queryRawResponseSize);

Exit:
    if (request.dnsQueryRaw != NULL)
    {
        HeapFree(GetProcessHeap(), 0, request.dnsQueryRaw);
        request.dnsQueryRaw = NULL;
    }

    if (context.queryResults != NULL)
    {
        DnsQueryRawResultFree(context.queryResults);
        context.queryResults = NULL;
    }

    if (context.event != NULL)
    {
        CloseHandle(context.event);
        context.event = NULL;
    }

    return errorStatus;
}
```

### Example 2

In this example, the query is initiated with a query name and type, but is then cancelled with [DnsCancelQueryRaw](./nf-windns-dnscancelqueryraw.md).

```cppwinrt
struct QUERY_RAW_CALLBACK_CONTEXT
{
    DNS_QUERY_RAW_RESULT    *queryResults;
    HANDLE                  event;
};

VOID
CALLBACK
QueryRawCallback(
    _In_    VOID                  *queryContext,
    _In_    DNS_QUERY_RAW_RESULT  *queryResults
)
{
    QUERY_RAW_CALLBACK_CONTEXT *context = static_cast<QUERY_RAW_CALLBACK_CONTEXT *>(queryContext);

    //
    //  Capture the results of the query. Note that this structure needs to
    //  be freed later with DnsQueryRawResultFree.
    //

    context->queryResults = queryResults;

    SetEvent(context->event);
}

DWORD
CallDnsQueryRawAndCancel(
    _In_    PWSTR                       queryName,
    _In_    USHORT                      queryType,
    _In_    ULONG                       interfaceIndex,
    _In_    SOCKADDR_INET               *sourceAddr,
    _In_    ULONG                       protocol,
    _In_    DNS_CUSTOM_SERVER           *customServers,
    _In_    ULONG                       customServersSize,
    _Inout_ QUERY_RAW_CALLBACK_CONTEXT  *context
)
{
    DWORD errorStatus = ERROR_SUCCESS;
    DWORD waitStatus = 0;
    DNS_QUERY_RAW_REQUEST request = {0};
    DNS_QUERY_RAW_CANCEL cancel = {0};

    request.version = DNS_QUERY_RAW_REQUEST_VERSION1;
    request.resultsVersion = DNS_QUERY_RAW_RESULTS_VERSION1; 
    request.dnsQueryRawSize = 0;
    request.dnsQueryRaw = NULL;
    request.dnsQueryName = queryName;
    request.dnsQueryType = queryType;
    request.queryOptions = DNS_QUERY_BYPASS_CACHE;
    request.interfaceIndex = interfaceIndex;
    request.queryCompletionCallback = &QueryRawCallback;
    request.queryContext = context;
    request.queryRawOptions = 0;
    request.customServersSize = customServersSize;
    request.customServers = customServers;
    request.protocol = protocol;
    request.sourceAddr = *sourceAddr;

    errorStatus = DnsQueryRaw(&request, &cancel);
    if (errorStatus != DNS_REQUEST_PENDING)
    {
        goto Exit;
    }

    //
    //  Cancel the query with the provided cancel handle.
    //

    errorStatus = DnsCancelQueryRaw(&cancel);
    if (errorStatus != ERROR_SUCCESS)
    {
        goto Exit;
    }

    //
    //  Wait for the callback to indicate that the query has completed. Note that it
    //  is possible for the query to complete successfully or fail for another reason
    //  before the DnsCancelQueryRaw call is made, so the queryStatus member of
    //  DNS_QUERY_RAW_RESULT can be used to determine what happened.
    //

    waitStatus = WaitForSingleObject(context->event, INFINITE);
    if (waitStatus != WAIT_OBJECT_0)
    {
        errorStatus = GetLastError();
        goto Exit;
    }

    errorStatus = context.queryResults->queryStatus;

    if (errorStatus == ERROR_CANCELLED)
    {
        //
	    //  DNS query was successfully cancelled.
	    //
    }	
    else if (errorStatus != ERROR_SUCCESS)
    {
        //
	    //  DNS query failed before it was cancelled.
	    //
    }
    else
    {
        //
	    //  DNS query succeeded before it was cancelled, and can contain valid results.
        //  The other fields of context.queryResults to be processed as in Example 1.
	    //
    }

    //
    //  The context is owned by the caller of this function, and it will be cleaned up there.
    //

Exit:
    return errorStatus;
}
```

## -see-also
