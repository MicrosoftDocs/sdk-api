---
UID: NS:mstcpip._ASSOCIATE_NAMERES_CONTEXT_INPUT
title: ASSOCIATE_NAMERES_CONTEXT_INPUT (mstcpip.h)
description: Contains the transport setting ID and handle to a fully qualified domain name.
helpviewer_keywords: ["*PASSOCIATE_NAMERES_CONTEXT_INPUT","ASSOCIATE_NAMERES_CONTEXT_INPUT","ASSOCIATE_NAMERES_CONTEXT_INPUT structure [Winsock]","PASSOCIATE_NAMERES_CONTEXT_INPUT","PASSOCIATE_NAMERES_CONTEXT_INPUT structure pointer [Winsock]","mstcpip/ASSOCIATE_NAMERES_CONTEXT_INPUT","mstcpip/PASSOCIATE_NAMERES_CONTEXT_INPUT","winsock.associate_nameres_context_input"]
old-location: winsock\associate_nameres_context_input.htm
tech.root: WinSock
ms.assetid: 8B6EB9A4-47B9-40C3-B647-BB05B657B7CE
ms.date: 12/05/2018
ms.keywords: '*PASSOCIATE_NAMERES_CONTEXT_INPUT, ASSOCIATE_NAMERES_CONTEXT_INPUT, ASSOCIATE_NAMERES_CONTEXT_INPUT structure [Winsock], PASSOCIATE_NAMERES_CONTEXT_INPUT, PASSOCIATE_NAMERES_CONTEXT_INPUT structure pointer [Winsock], mstcpip/ASSOCIATE_NAMERES_CONTEXT_INPUT, mstcpip/PASSOCIATE_NAMERES_CONTEXT_INPUT, winsock.associate_nameres_context_input'
req.header: mstcpip.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: ASSOCIATE_NAMERES_CONTEXT_INPUT, *PASSOCIATE_NAMERES_CONTEXT_INPUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ASSOCIATE_NAMERES_CONTEXT_INPUT
 - mstcpip/_ASSOCIATE_NAMERES_CONTEXT_INPUT
 - PASSOCIATE_NAMERES_CONTEXT_INPUT
 - mstcpip/PASSOCIATE_NAMERES_CONTEXT_INPUT
 - ASSOCIATE_NAMERES_CONTEXT_INPUT
 - mstcpip/ASSOCIATE_NAMERES_CONTEXT_INPUT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mstcpip.h
api_name:
 - ASSOCIATE_NAMERES_CONTEXT_INPUT
---

# ASSOCIATE_NAMERES_CONTEXT_INPUT structure


## -description



The <b>ASSOCIATE_NAMERES_CONTEXT_INPUT</b> structure contains the transport setting ID and handle to a fully qualified domain name.

## -struct-fields

### -field TransportSettingId

The transport setting ID.

### -field Handle

Handle to a fully qualified domain name.

## -remarks

Generally speaking, you can use <b>ASSOCIATE_NAMERES_CONTEXT_INPUT</b> to enforce policy based on Fully Qualified Domain Name (FQDN), rather than just IP address. you can do so by retrieving a handle to a FQDN with a call to <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a>, using the addinfoex4 structure.  From there, you can use the handle in <b>ASSOCIATE_NAMERES_CONTEXT_INPUT</b> in a call to <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a>, using the             <b>SIO_APPLY_TRANSPORT_SETTING</b> ioctl.


#### Examples

The following code describes making a call to <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a> with a addinfoex4 structure to retrieve the handle to a FQDN. the sample then call <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> with the <b>ASSOCIATE_NAMERES_CONTEXT_INPUT</b> structure.


```cpp
// 
// Connect to a server using its IPv4 addresses 
// 

VOID 
ConnectServer( 
    PCWSTR server) 
{ 
    int iResult; 
    PADDRINFOEX4 pResult = NULL; 
    ADDRINFOEX3 hints = { 0 }; 
    PADDRINFOEX4 pCur = NULL; 
    WSADATA wsaData; 
    SOCKET connectSocket = INVALID_SOCKET; 
    ULONG bytesReturned = 0; 
    ASSOCIATE_NAMERES_CONTEXT_INPUT input = { 0 }; 
    SOCKADDR_IN clientService; 
    wchar_t ipstringbuffer[46]; 
    String string; 
    DWORD dwRetval; 
    //  
    //  Initialize Winsock 
    // 
    iResult = WSAStartup( 
        MAKEWORD(2, 2),  
        &wsaData); 
    if (iResult != 0) { 
        printf("WSAStartup failed: %d\n", iResult); 
        goto Exit; 
    } 

    //  
    // Create a SOCKET for connection 
    // 
    connectSocket = socket( 
        AF_UNSPEC,  
        SOCK_STREAM,  
        IPPROTO_TCP); 
    if (connectSocket == INVALID_SOCKET)  
    { 
        printf("socket failed: %d\n", WSAGetLastError()); 
        goto Exit; 
    } 

    // 
    // Do name resolution 
    // 

    hints.ai_family = AF_INET; 
    hints.ai_socktype = SOCK_STREAM; 
    hints.ai_flags = AI_EXTENDED | AI_FQDN | AI_CANONNAME | AI_RESOLUTION_HANDLE; 
    hints.ai_version = ADDRINFOEX_VERSION_4; 

    dwRetval = GetAddrInfoExW( 
        server, 
        NULL, 
        NS_DNS, 
        NULL, 
        (const ADDRINFOEXW*)&hints, 
        (PADDRINFOEXW*)&pResult, 
        NULL, 
        NULL, 
        NULL, NULL); 
    if (dwRetval != 0) { 
        printf("GetAddrInfoEx failed with error: %d\n", dwRetval); 
        goto Exit; 
    } 
    input.TransportSettingId.Guid = ASSOCIATE_NAMERES_CONTEXT; 
    input.Handle = pResult->ai_resolutionhandle; 

    // 
    // Associate socket with the handle 
    // 

    if (WSAIoctl( 
            connectSocket, 
            SIO_APPLY_TRANSPORT_SETTING, 
            (VOID *)&input, 
            sizeof(input), 
            NULL, 
            0, 
            &bytesReturned, 
            NULL, 
            NULL) == SOCKET_ERROR) 
    if (iResult != 0){ 
        printf("WSAIoctl failed: %d\n", WSAGetLastError()); 
        goto Exit; 
    }     

    // 
    // Connect to server 
    // 

    pCur = pResult; 
    while (pCur != NULL) 
    { 
        if (pCur->ai_addr->sa_family == AF_INET) 
        { 
            clientService = *(const sockaddr_in*)pCur->ai_addr; 
            clientService.sin_port = htons(80); 
            if (connect( 
                connectSocket, 
                (const SOCKADDR *)&clientService, 
                sizeof(clientService)) == SOCKET_ERROR) 
            { 
                printf("connect failed: %d\n", WSAGetLastError()); 
                goto Exit; 
            } 
        } 
        pCur = pCur->ai_next; 
    } 

Exit: 

    if (connectSocket != INVALID_SOCKET) 
    { 
        closesocket(connectSocket); 
    } 
    if (pResult) 
    { 
        FreeAddrInfoExW((ADDRINFOEXW*)pResult); 
    } 
    WSACleanup(); 
    return; 
} 

```

## -see-also

<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoex4">addrinfoex4</a>