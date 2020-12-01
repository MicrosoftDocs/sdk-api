---
UID: NF:lmaccess.NetGetDCName
title: NetGetDCName function (lmaccess.h)
description: The NetGetDCName function returns the name of the primary domain controller (PDC). It does not return the name of the backup domain controller (BDC) for the specified domain. Also, you cannot remote this function to a non-PDC server.
helpviewer_keywords: ["NetGetDCName","NetGetDCName function [Network Management]","_win32_netgetdcname","lmaccess/NetGetDCName","netmgmt.netgetdcname"]
old-location: netmgmt\netgetdcname.htm
tech.root: NetMgmt
ms.assetid: 3e32aacc-088e-455a-bc1b-92274e98d2e5
ms.date: 12/05/2018
ms.keywords: NetGetDCName, NetGetDCName function [Network Management], _win32_netgetdcname, lmaccess/NetGetDCName, netmgmt.netgetdcname
req.header: lmaccess.h
req.include-header: Lm.h
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
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetGetDCName
 - lmaccess/NetGetDCName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetGetDCName
---

# NetGetDCName function


## -description

The
				<b>NetGetDCName</b> function returns the name of the primary domain controller (PDC). It does not return the name of the backup domain controller (BDC) for the specified domain. Also, you cannot remote this function to a non-PDC server.

Applications that support DNS-style names should call the 
<a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName</a> function. Domain controllers in this type of environment have a multi-master directory replication relationship. Therefore, it may be advantageous for your application to use a DC that is not the PDC. You can call the <b>DsGetDcName</b> function to locate any DC in the domain; 
<b>NetGetDCName</b> returns only the name of the PDC.

## -parameters

### -param servername [in]

A pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param domainname [in]

A pointer to a constant string that specifies the name of the domain. The domain name must be a NetBIOS domain name (for example, microsoft). 
<b>NetGetDCName</b> does not support DNS-style names (for example, microsoft.com). If this parameter is <b>NULL</b>, the function returns the name of the domain controller for the primary domain.

### -param bufptr [out]

A pointer to an allocated buffer that receives a string that specifies the server name of the PDC of the domain. The server name is returned as Unicode string prefixed by \\. This buffer is allocated by the system and must be freed using the 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a> and 
<a href="/windows/desktop/NetMgmt/network-management-function-buffer-lengths">Network Management Function Buffer Lengths</a>.

## -returns

If the function succeeds, the return value is NERR_Success.

If the function fails, the return value can be one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_DCNotFound</b></dt>
</dl>
</td>
<td width="60%">
Could not find the domain controller for the domain specified in the <i>domainname</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_NETPATH</b></dt>
</dl>
</td>
<td width="60%">
The network path was not found. This error is returned if the computer specified in the <i>servername</i> parameter could not be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_NAME</b></dt>
</dl>
</td>
<td width="60%">
The name syntax is incorrect. This error is returned if the name specified in the <i>servername</i> parameter contains illegal characters. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. 

</td>
</tr>
</table>

## -remarks

No special group membership is required to successfully execute the 
<b>NetGetDCName</b> function.


#### Examples

The following code sample demonstrates how to retrieve the primary domain controller using the  
<b>NetGetDCName</b> function. The sample calls 
<b>NetGetDCName</b> specifying the servername and domainname parameters. If the call succeeds, the code prints information out the name of the primary domain controller. Finally, the sample frees the memory allocated for the buffer where the domain controller name was returned.


```cpp
#ifndef UNICODE
#define UNICODE
#endif

#include <stdio.h>
#include <stdlib.h>  // for _wtoi function
#include <assert.h>
#include <windows.h>
#include <lm.h>

// Need to link with netapi32.lib
#pragma comment(lib, "netapi32.lib")

int wmain(int argc, wchar_t * argv[])
{

    NET_API_STATUS nStatus;

    LPCWSTR lpServer = NULL;
    LPCWSTR lpDomain = NULL;

    LPCWSTR lpDcName = NULL;
    
    if (argc != 3 ) {
        wprintf(L"Usage: %ws <ServerName> <DomainName>\n",
                argv[0]);
        wprintf(L"     %ws Myserver Domain\n", argv[0]);
        exit(1);
    }

    lpServer = argv[1];
    lpDomain = argv[2];

    wprintf(L"Calling NetGetDCName with parameters\n");
    wprintf(L"    lpServer = %ws\n", lpServer);
    wprintf(L"    lpDomain = %ws\n", lpDomain);

    //
    // Call the NetGetDCName function
    //
    nStatus = NetGetDCName(lpServer, lpDomain, (LPBYTE *) &lpDcName);
    //
    // If the call succeeds,
    //
    if (nStatus == NERR_Success) {
        wprintf(L"NetGetDCName was successful\n", nStatus);
        wprintf(L"DC Name = %ws\n", lpDcName);
        // Need to free the returned buffer
        nStatus = NetApiBufferFree( (LPVOID) lpDcName);
        if (nStatus != NERR_Success)
            wprintf(L"NetApiBufferFree failed with error: %lu (0x%lx)\n",
                nStatus, nStatus);
    } else {
        wprintf(L"NetGetDCName failed with error: %lu (0x%lx)\n", nStatus,
                nStatus);
        wprintf(L"   Error = ");
        switch (nStatus) {
        case ERROR_INVALID_PARAMETER:
            wprintf(L"ERROR_INVALID_PARAMETER\n");
            break;
        case ERROR_NO_SUCH_DOMAIN:
            wprintf(L"ERROR_NO_SUCH_DOMAIN\n");
            break;
        case ERROR_NOT_SUPPORTED:
            wprintf(L"ERROR_NOT_SUPPORTED\n");
            break;
        case ERROR_BAD_NETPATH:
            wprintf(L"ERROR_BAD_NETPATH\n");
            break;
        case ERROR_INVALID_COMPUTERNAME:
            wprintf(L"ERROR_INVALID_COMPUTERNAME\n");
            break;
        case DNS_ERROR_INVALID_NAME_CHAR:
            wprintf(L"DNS_ERROR_INVALID_NAME_CHAR\n");
            break;
        case DNS_ERROR_NON_RFC_NAME:
            wprintf(L"DNS_ERROR_NON_RFC_NAME\n");
            break;
        case ERROR_INVALID_NAME:
            wprintf(L"ERROR_INVALID_NAME\n");
            break;
        case NERR_DCNotFound:
            wprintf(L"NERR_DCNotFound\n");
            break;
        case NERR_WkstaNotStarted:
            wprintf(L"NERR_WkstaNotStarted\n");
            break;
        case RPC_S_SERVER_UNAVAILABLE:
            wprintf(L"RPC_S_SERVER_UNAVAILABLE\n");
            break;
        case RPC_E_REMOTE_DISABLED:
            wprintf(L"RPC_E_REMOTE_DISABLED\n");
            break;
        default:
            wprintf(L"Other error, see Winerror.h or lmerr.h)\n");
            break;
        }
    }

    return nStatus;
}

```

## -see-also

<a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName</a>



<a href="/windows/desktop/NetMgmt/get-functions">Get Functions</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgetanydcname">NetGetAnyDCName</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>