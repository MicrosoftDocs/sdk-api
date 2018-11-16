---
UID: NS:mstcpip._ASSOCIATE_NAMERES_CONTEXT_INPUT
title: "_ASSOCIATE_NAMERES_CONTEXT_INPUT"
author: windows-sdk-content
description: Contains the transport setting ID and handle to a fully qualified domain name.
old-location: winsock\associate_nameres_context_input.htm
tech.root: WinSock
ms.assetid: 8B6EB9A4-47B9-40C3-B647-BB05B657B7CE
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PASSOCIATE_NAMERES_CONTEXT_INPUT, ASSOCIATE_NAMERES_CONTEXT_INPUT, ASSOCIATE_NAMERES_CONTEXT_INPUT structure [Winsock], PASSOCIATE_NAMERES_CONTEXT_INPUT, PASSOCIATE_NAMERES_CONTEXT_INPUT structure pointer [Winsock], _ASSOCIATE_NAMERES_CONTEXT_INPUT, mstcpip/ASSOCIATE_NAMERES_CONTEXT_INPUT, mstcpip/PASSOCIATE_NAMERES_CONTEXT_INPUT, winsock.associate_nameres_context_input"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mstcpip.h
api_name:
 - ASSOCIATE_NAMERES_CONTEXT_INPUT
product: Windows
targetos: Windows
req.typenames: ASSOCIATE_NAMERES_CONTEXT_INPUT, *PASSOCIATE_NAMERES_CONTEXT_INPUT
req.redist: 
---

# _ASSOCIATE_NAMERES_CONTEXT_INPUT structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

The <b>ASSOCIATE_NAMERES_CONTEXT_INPUT</b> structure contains the transport setting ID and handle to a fully qualified domain name.


## -struct-fields




### -field TransportSettingId

The transport setting ID.


### -field Handle

Handle to a fully qualified domain name.


## -remarks



Generally speaking, you can use <b>ASSOCIATE_NAMERES_CONTEXT_INPUT</b> to enforce policy based on Fully Qualified Domain Name (FQDN), rather than just IP address. you can do so by retrieving a handle to a FQDN with a call to <a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a>, using the addinfoex4 structure.  From there, you can use the handle in <b>ASSOCIATE_NAMERES_CONTEXT_INPUT</b> in a call to <a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a>, using the             <b>SIO_APPLY_TRANSPORT_SETTING</b> ioctl.


#### Examples

The following code describes making a call to <a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a> with a addinfoex4 structure to retrieve the handle to a FQDN. the sample then call <a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a> with the <b>ASSOCIATE_NAMERES_CONTEXT_INPUT</b> structure.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// 
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
        &amp;wsaData); 
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
        (const ADDRINFOEXW*)&amp;hints, 
        (PADDRINFOEXW*)&amp;pResult, 
        NULL, 
        NULL, 
        NULL, NULL); 
    if (dwRetval != 0) { 
        printf("GetAddrInfoEx failed with error: %d\n", dwRetval); 
        goto Exit; 
    } 
    input.TransportSettingId.Guid = ASSOCIATE_NAMERES_CONTEXT; 
    input.Handle = pResult-&gt;ai_resolutionhandle; 

    // 
    // Associate socket with the handle 
    // 

    if (WSAIoctl( 
            connectSocket, 
            SIO_APPLY_TRANSPORT_SETTING, 
            (VOID *)&amp;input, 
            sizeof(input), 
            NULL, 
            0, 
            &amp;bytesReturned, 
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
        if (pCur-&gt;ai_addr-&gt;sa_family == AF_INET) 
        { 
            clientService = *(const sockaddr_in*)pCur-&gt;ai_addr; 
            clientService.sin_port = htons(80); 
            if (connect( 
                connectSocket, 
                (const SOCKADDR *)&amp;clientService, 
                sizeof(clientService)) == SOCKET_ERROR) 
            { 
                printf("connect failed: %d\n", WSAGetLastError()); 
                goto Exit; 
            } 
        } 
        pCur = pCur-&gt;ai_next; 
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a>



<a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a>



<a href="https://msdn.microsoft.com/96B19008-9F20-4F47-A0F1-AA695227725B">addrinfoex4</a>
 

 

