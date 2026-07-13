---
UID: NF:winsock2.WSAEnumNameSpaceProvidersA
title: WSAEnumNameSpaceProvidersA function (winsock2.h)
description: The WSAEnumNameSpaceProviders function retrieves information on available namespace providers. (ANSI)
helpviewer_keywords: ["WSAEnumNameSpaceProvidersA", "winsock2/WSAEnumNameSpaceProvidersA"]
old-location: winsock\wsaenumnamespaceproviders_2.htm
tech.root: WinSock
ms.assetid: f5b6cd42-c5cb-43b6-bb96-fd260217e252
ms.date: 12/05/2018
ms.keywords: WSAEnumNameSpaceProviders, WSAEnumNameSpaceProviders function [Winsock], WSAEnumNameSpaceProvidersA, WSAEnumNameSpaceProvidersW, _win32_wsaenumnamespaceproviders_2, winsock.wsaenumnamespaceproviders_2, winsock2/WSAEnumNameSpaceProviders, winsock2/WSAEnumNameSpaceProvidersA, winsock2/WSAEnumNameSpaceProvidersW
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WSAEnumNameSpaceProvidersW (Unicode) and WSAEnumNameSpaceProvidersA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WSAEnumNameSpaceProvidersA
 - winsock2/WSAEnumNameSpaceProvidersA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - WSAEnumNameSpaceProviders
 - WSAEnumNameSpaceProvidersA
 - WSAEnumNameSpaceProvidersW
---

# WSAEnumNameSpaceProvidersA function


## -description

The 
<b>WSAEnumNameSpaceProviders</b> function retrieves information on available namespace providers.

## -parameters

### -param lpdwBufferLength [in, out]

On input, the number of bytes contained in the buffer pointed to by <i>lpnspBuffer</i>. On output (if the function fails, and the error is 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a>), the minimum number of bytes to pass for the <i>lpnspBuffer</i> to retrieve all the requested information. The buffer passed to <b>WSAEnumNameSpaceProviders</b> must be sufficient to hold all of the namespace information.

### -param lpnspBuffer [out]

A buffer that is filled with 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsanamespace_infow">WSANAMESPACE_INFO</a> structures. The returned structures are located consecutively at the head of the buffer. Variable sized information referenced by pointers in the structures point to locations within the buffer located between the end of the fixed sized structures and the end of the buffer. The number of structures filled in is the return value of 
<b>WSAEnumNameSpaceProviders</b>.

## -returns

The 
<b>WSAEnumNameSpaceProviders</b> function returns the number of 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsanamespace_infow">WSANAMESPACE_INFO</a> structures copied into <i>lpnspBuffer</i>. Otherwise, the value SOCKET_ERROR is returned, and a specific error number can be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpnspBuffer</i> parameter was a <b>NULL</b> pointer or the buffer length, <i>lpdwBufferLength</i>, was too small to receive all the relevant 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsanamespace_infow">WSANAMESPACE_INFO</a> structures and associated information. When this error is returned, the buffer length required is returned in the <i>lpdwBufferLength</i> parameter. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
The WS2_32.DLL has not been initialized. The application must first call 
<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a> before calling any Windows Sockets functions.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to perform the operation.

</td>
</tr>
</table>

## -remarks

The <b>WSAEnumNameSpaceProviders</b> function returns information on available namespace providers in the buffer pointed to by the <i>lpnspBuffer</i> parameter. The returned buffer contains an array of <a href="/windows/desktop/api/winsock2/ns-winsock2-wsanamespace_infow">WSANAMESPACE_INFO</a> structures located consecutively at the head of the buffer. Variable sized information referenced by pointers in the <b>WSANAMESPACE_INFO</b> structures point to locations within the buffer located between the end of the fixed <b>WSANAMESPACE_INFO</b> structures and the end of the buffer. The number of <b>WSANAMESPACE_INFO</b> structures filled in is returned by the  
<b>WSAEnumNameSpaceProviders</b> function.

Each <a href="/windows/desktop/api/winsock2/ns-winsock2-wsanamespace_infow">WSANAMESPACE_INFO</a>  structure entry contains the provider-specific information on the namespace entry
                     passed to the <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespace">WSCInstallNameSpace</a> and <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespace32">WSCInstallNameSpace32</a> functions when the namespace provider was installed.

The <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersexa">WSAEnumNameSpaceProvidersEx</a>  function is an enhanced version of the <b>WSAEnumNameSpaceProviders</b> function. The  <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32">WSCEnumNameSpaceProvidersEx32</a> function is an enhanced version of the <b>WSAEnumNameSpaceProviders</b> function that returns information on available 32-bit namespace providers for use on 64-bit platforms.

<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
The following example demonstrates the use of the <b>WSAEnumNameSpaceProviders</b> function to retrieve information on available namespace providers.


```cpp
#ifndef UNICODE
#define UNICODE 1
#endif

#include <winsock2.h>
#include <ws2tcpip.h>
#include <objbase.h>
#include <stdio.h>

// Link with ws2_32.lib and ole32.lib
#pragma comment (lib, "Ws2_32.lib")
#pragma comment (lib, "ole32.lib")

#define MALLOC(x) HeapAlloc(GetProcessHeap(), 0, (x))
#define FREE(x) HeapFree(GetProcessHeap(), 0, (x))
// Note: could also use malloc() and free()

int wmain()
{

    //-----------------------------------------
    // Declare and initialize variables
    WSADATA wsaData;
    int iResult;
    int iError = 0;

    INT iNuminfo = 0;

    int i;
    

    // Allocate a 4K buffer to retrieve all the namespace providers
    DWORD dwInitialBufferLen = 4096;
    DWORD dwBufferLen;
    LPWSANAMESPACE_INFO lpProviderInfo;
    
    
    // variables needed for converting provider GUID to a string
    int iRet = 0;
    WCHAR GuidString[40] = {0};

    // Set dwBufferLen to the initial buffer length
    dwBufferLen = dwInitialBufferLen;
    
    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed: %d\n", iResult);
        return 1;
    }
    
    lpProviderInfo = (LPWSANAMESPACE_INFO) MALLOC(dwBufferLen);
    if (lpProviderInfo == NULL) {
        wprintf(L"Memory allocation for providers buffer failed\n");
        WSACleanup();
        return 1;
    }
    
    iNuminfo = WSAEnumNameSpaceProviders(&dwBufferLen, lpProviderInfo);
    if (iNuminfo == SOCKET_ERROR) {
        iError = WSAGetLastError();
        if (iError == WSAEFAULT && dwBufferLen != dwInitialBufferLen) {
            wprintf(L"WSAEnumNameSpaceProviders failed with too small a buffer\n");
            wprintf(L"  Increasing the buffer to %u\n\n", dwBufferLen);
            if (lpProviderInfo) {
               FREE(lpProviderInfo);
               lpProviderInfo = NULL;
            }        

            lpProviderInfo = (LPWSANAMESPACE_INFO) MALLOC(dwBufferLen);
            if (lpProviderInfo == NULL) {
                wprintf(L"Memory allocation for providers buffer failed\n");
                WSACleanup();
               return 1;
            }

            iNuminfo = WSAEnumNameSpaceProviders(&dwBufferLen, lpProviderInfo);
            if (iNuminfo == SOCKET_ERROR) {
               wprintf(L"WSAEnumNameSpaceProviders failed with error: %d\n",
                  WSAGetLastError() );
               if (lpProviderInfo) {
                  FREE(lpProviderInfo);
                  lpProviderInfo = NULL;
               }        
               WSACleanup();
               return 1;
            }
            else
                wprintf(L"\n");   
        } 
        else {   
            wprintf(L"WSAEnumNameSpaceProviders failed with error: %d\n",
               WSAGetLastError() );
            if (lpProviderInfo) {
               FREE(lpProviderInfo);
               lpProviderInfo = NULL;
            }        
           WSACleanup();
           return 1;
        } 
     }

       wprintf(L"WSAEnumNameSpaceProviders succeeded with provider data count = %d\n\n",
           iNuminfo);
       for (i= 0; i < iNuminfo; i++) {
            iRet = StringFromGUID2(lpProviderInfo[i].NSProviderId, (LPOLESTR) &GuidString, 39); 
            if (iRet == 0)
                wprintf(L"StringFromGUID2 failed\n");
            else 
                wprintf(L"NameSpace ProviderId[%u] = %ws\n",i, GuidString);

           wprintf(L"NameSpace[%u] = ", i);
           switch (lpProviderInfo[i].dwNameSpace) {
           case NS_DNS:
               wprintf(L"Domain Name System (NS_DNS)\n");
               break;
           case NS_WINS:
               wprintf(L"Windows Internet Naming Service (NS_WINS)\n");
               break;
           case NS_NETBT:
               wprintf(L"NetBIOS (NS_NETBT)\n");
               break;
           case NS_NTDS:
               wprintf(L"Windows NT Directory Services (NS_NTDS)\n");
               break;
           case NS_NLA:
               wprintf(L"Network Location Awareness (NS_NLA)\n");
               break;
           // following values only defined on Vista and later
#if(_WIN32_WINNT >= 0x0600)
           case NS_BTH:
               wprintf(L"Bluetooth (NS_BTH)\n");
               break;
           case NS_EMAIL:
               wprintf(L"Email (NS_EMAIL)\n");
               break;
           case NS_PNRPNAME:
               wprintf(L"Peer-to-peer (NS_PNRPNAME)\n");
               break;
           case NS_PNRPCLOUD:
               wprintf(L"Peer-to-peer collection (NS_PNRPCLOUD)\n");
               break;
#endif
           default:
               wprintf(L"Other value (%u)\n", lpProviderInfo[i].dwNameSpace);             
               break;
           }    

           if (lpProviderInfo[i].fActive)
               wprintf(L"Namespace[%u] is active\n", i);
           else    
               wprintf(L"Namespace[%u] is inactive\n", i);

           wprintf(L"NameSpace Version[%u] = %u\n", i, lpProviderInfo[i].dwVersion);

           wprintf(L"Namespace Identifier[%u] = %ws\n\n", i, lpProviderInfo[i].lpszIdentifier);
       }           

    if (lpProviderInfo) {
        FREE(lpProviderInfo);
        lpProviderInfo = NULL;
    }        
    WSACleanup();
    
    return 0;
}

```


<b>Windows Phone 8:</b> The <b>WSAEnumNameSpaceProvidersW</b> function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: The <b>WSAEnumNameSpaceProvidersW</b> function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.





> [!NOTE]
> The winsock2.h header defines WSAEnumNameSpaceProviders as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersexa">WSAEnumNameSpaceProvidersEx</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-wsanamespace_infow">WSANAMESPACE_INFO</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32">WSCEnumNameSpaceProvidersEx32</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespace">WSCInstallNameSpace</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespaceex">WSCInstallNameSpaceEx</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>
