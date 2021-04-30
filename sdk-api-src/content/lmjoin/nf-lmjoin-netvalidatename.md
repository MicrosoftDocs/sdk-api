---
UID: NF:lmjoin.NetValidateName
title: NetValidateName function (lmjoin.h)
description: The NetValidateName function verifies that a name is valid for name type specified(computer name, workgroup name, domain name, or DNS computer name).
helpviewer_keywords: ["NetSetupDnsMachine","NetSetupDomain","NetSetupMachine","NetSetupNonExistentDomain","NetSetupUnknown","NetSetupWorkgroup","NetValidateName","NetValidateName function [Network Management]","_win32_netvalidatename","lmjoin/NetValidateName","netmgmt.netvalidatename"]
old-location: netmgmt\netvalidatename.htm
tech.root: NetMgmt
ms.assetid: 772603df-ec17-4a83-a715-2d9a14d5c2bb
ms.date: 12/05/2018
ms.keywords: NetSetupDnsMachine, NetSetupDomain, NetSetupMachine, NetSetupNonExistentDomain, NetSetupUnknown, NetSetupWorkgroup, NetValidateName, NetValidateName function [Network Management], _win32_netvalidatename, lmjoin/NetValidateName, netmgmt.netvalidatename
req.header: lmjoin.h
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
 - NetValidateName
 - lmjoin/NetValidateName
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
 - NetValidateName
---

# NetValidateName function


## -description

The
				<b>NetValidateName</b> function verifies that a name is valid for name type specified(computer name, workgroup name, domain name, or DNS computer name).

## -parameters

### -param lpServer [in]

A pointer to a constant string that specifies the DNS or NetBIOS name of the computer on which to call the function. If this parameter is <b>NULL</b>, the local computer is used.

### -param lpName [in]

A pointer to a constant string that specifies the name to validate. Depending on the value specified in the <i>NameType</i> parameter, the <i>lpName</i>  parameter can point to a computer name, workgroup name, domain name, or DNS computer name.

### -param lpAccount [in]

If the <i>lpName</i> parameter is a domain name, this parameter points to an account name to use when connecting to the domain controller. The string must specify either a domain NetBIOS name and user account (for example, "REDMOND\user") or the user principal name (UPN) of the user in the form of an Internet-style login name (for example, "someone@example.com"). If this parameter is <b>NULL</b>, the caller's context is used.

### -param lpPassword [in]

If the <i>lpAccount</i>  parameter specifies an account name, this parameter must point to the password to use when connecting to the domain controller. Otherwise, this parameter must be <b>NULL</b>.

### -param NameType [in]

The type of the name passed in the <i>lpName</i> parameter to validate. This parameter can be one of the values from the NETSETUP_NAME_TYPE enumeration type defined in the <i>Lmjoin.h</i> header file.

Note that the <i>Lmjoin.h</i> header is automatically included by the <i>Lm.h</i> header file. The <i>Lmjoin.h</i> header files should not be used directly. 



 The following list shows the possible values for this parameter. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NetSetupUnknown"></a><a id="netsetupunknown"></a><a id="NETSETUPUNKNOWN"></a><dl>
<dt><b>NetSetupUnknown</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The nametype is unknown. If this value is used, the <b>NetValidateName</b> function fails with <b>ERROR_INVALID_PARAMETER</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="NetSetupMachine"></a><a id="netsetupmachine"></a><a id="NETSETUPMACHINE"></a><dl>
<dt><b>NetSetupMachine</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Verify that the NetBIOS computer name is valid and that it is not in use.

</td>
</tr>
<tr>
<td width="40%"><a id="NetSetupWorkgroup"></a><a id="netsetupworkgroup"></a><a id="NETSETUPWORKGROUP"></a><dl>
<dt><b>NetSetupWorkgroup</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Verify that the workgroup name is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="NetSetupDomain"></a><a id="netsetupdomain"></a><a id="NETSETUPDOMAIN"></a><dl>
<dt><b>NetSetupDomain</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Verify that the domain name exists and that it is a domain.

</td>
</tr>
<tr>
<td width="40%"><a id="NetSetupNonExistentDomain"></a><a id="netsetupnonexistentdomain"></a><a id="NETSETUPNONEXISTENTDOMAIN"></a><dl>
<dt><b>NetSetupNonExistentDomain</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Verify that the domain name is not in use.

</td>
</tr>
<tr>
<td width="40%"><a id="NetSetupDnsMachine"></a><a id="netsetupdnsmachine"></a><a id="NETSETUPDNSMACHINE"></a><dl>
<dt><b>NetSetupDnsMachine</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Verify that the DNS computer name is valid.

This value is supported on Windows 2000 and later. The application must be compiled with <b>_WIN32_WINNT &gt;= 0x0500</b> to use this value.

</td>
</tr>
</table>

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
<dt><b>DNS_ERROR_INVALID_NAME_CHAR</b></dt>
</dl>
</td>
<td width="60%">
The DNS name contains an invalid character. This error is returned if the <i>NameType</i> parameter specified is <b>NetSetupDnsMachine</b> and the DNS name in the <i>lpName</i> parameter contains an invalid character. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DNS_ERROR_NON_RFC_NAME</b></dt>
</dl>
</td>
<td width="60%">
The DNS name does not comply with RFC specifications. This error is returned if the  <i>NameType</i> parameter specified is <b>NetSetupDnsMachine</b> and the DNS name in the <i>lpName</i> parameter does not comply with RFC specifications. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DUP_NAME</b></dt>
</dl>
</td>
<td width="60%">
A duplicate name already exists on the network.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_COMPUTERNAME</b></dt>
</dl>
</td>
<td width="60%">
The format of the specified computer name is not valid. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is incorrect. This error is returned if the  <i>lpName</i> parameter is <b>NULL</b> or the <i>NameType</i> parameter is specified as <b>NetSetupUnknown</b> or an unknown nametype. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SUCH_DOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The specified domain does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if a remote computer was specified in the <i>lpServer</i> parameter and this call is not supported on the remote computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_InvalidComputer</b></dt>
</dl>
</td>
<td width="60%">
The specified computer name is not valid. This error is returned if the <i>NameType</i> parameter specified is <b>NetSetupDnsMachine</b> or <b>NetSetupMachine</b> and the specified computer name is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_InvalidWorkgroupName</b></dt>
</dl>
</td>
<td width="60%">
The specified workgroup name is not valid. This error is returned if the <i>NameType</i> parameter specified is <b>NetSetupWorkgroup</b> and the specified workgroup name is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_SERVER_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The RPC server is not available. This error is returned if a remote computer was specified in the <i>lpServer</i> parameter and the RPC server is not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_E_REMOTE_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
Remote calls are not allowed for this process. This error is returned if a remote computer was specified in the <i>lpServer</i> parameter and remote calls are not allowed for this process.

</td>
</tr>
</table>

## -remarks

The
				<b>NetValidateName</b> function validates a name based on the nametype specified. 

If the <i>NameType</i> parameter is <b>NetSetupMachine</b>, the name passed  in the <i>lpName</i> parameter must be syntactically correct as a NetBIOS name and the name must not currently be in use on the network.

If the <i>NameType</i> parameter is <b>NetSetupWorkgroup</b>, the name passed  in the <i>lpName</i> parameter must be syntactically correct as a NetBIOS name, the name must not currently be in use on the network as a unique name, and the name must be different from the computer name.

If the <i>NameType</i> parameter is <b>NetSetupDomain</b>, the name passed  in the <i>lpName</i> parameter must be syntactically correct as a NetBIOS or DNS name and the name must currently be registered as a domain name.

If the <i>NameType</i> parameter is <b>NetSetupNonExistentDomain</b>, the name passed  in the <i>lpName</i> parameter must be syntactically correct as a NetBIOS or DNS name and the name must currently not be registered as a domain name.

If the <i>NameType</i> parameter is <b>NetSetupDnsMachine</b>, the name passed  in the <i>lpName</i> parameter must be syntactically correct as a DNS name.

NetBIOS names are limited to maximum length of 16 characters.

No special group membership is required to successfully execute the 
<b>NetValidateName</b> function.


#### Examples

The following example validates a name for a specific type.


```cpp
#ifndef UNICODE
#define UNICODE
#endif
#pragma comment(lib, "netapi32.lib")

#include <stdio.h>
#include <stdlib.h>
#include <assert.h>
#include <windows.h>
#include <lm.h>

int wmain(int argc, wchar_t * argv[])
{

    NET_API_STATUS nStatus;

    LPCWSTR lpServer = NULL;
    LPCWSTR lpName = NULL;
    LPCWSTR lpAccount = NULL;
    LPCWSTR lpPassword = NULL;
    DWORD dwNameType = NetSetupUnknown; // unknown name type

    if (argc != 3 && argc != 4 && argc != 6) {
        wprintf(L"Usage: %ws Server Name AccountName Password> nametype\n",
                argv[0]);
        wprintf(L"Usage: %ws Server Name nametype\n", argv[0]);
        wprintf(L"Usage: %ws Name nametype\n", argv[0]);
        wprintf(L"     %ws Client2 2\n", argv[0]);
        wprintf(L"     %ws Myserver Client2 3\n", argv[0]);
        wprintf(L"     %ws Myserver Client2 domain\\user password 3\n", argv[0]);
        exit(1);
    }
    // The request is not for the primary domain.
    //
    if (argc == 3) {
        lpName = argv[1];
        dwNameType = _wtoi(argv[2]);
    }

    if (argc == 4) {
        lpServer = argv[1];
        lpName = argv[2];
        dwNameType = _wtoi(argv[3]);
    }

    if (argc == 6) {
        lpServer = argv[1];
        lpName = argv[2];
        lpAccount = argv[3];
        lpPassword = argv[4];
        dwNameType = _wtoi(argv[5]);
    }

    wprintf(L"Calling NetValidateName with parameters\n");
    wprintf(L"    lpServer = %ws\n", lpServer);
    wprintf(L"    lpName = %ws\n", lpName);
    wprintf(L"    lpAccount = %ws\n", lpAccount);
    wprintf(L"    lpPassword = %ws\n", lpPassword);
    wprintf(L"    NameType  = %d ", dwNameType);
    switch (dwNameType) {
    case NetSetupUnknown:
        wprintf(L"(NetSetupUnknown)\n");
        break;
    case NetSetupMachine:
        wprintf(L"(NetSetupMachine)\n");
        break;
    case NetSetupWorkgroup:
        wprintf(L"(NetSetupWorkgroup)\n");
        break;
    case NetSetupDomain:
        wprintf(L"(NetSetupDomain)\n");
        break;
    case NetSetupNonExistentDomain:
        wprintf(L"(NetSetupNonExistentDomain)\n");
        break;
#if(_WIN32_WINNT >= 0x0500)
    case NetSetupDnsMachine:
        wprintf(L"(NetSetupDnsMachine)\n");
        break;
#endif
    default:
        wprintf(L"Other unknown nametype)\n");
        break;
    }

    //
    // Call the NetValidateName function to validate the name
    //
    nStatus = NetValidateName(lpServer,
                              lpName, lpAccount, lpPassword, (NETSETUP_NAME_TYPE) dwNameType);
    //
    // If the call succeeds,
    //
    if ((nStatus == NERR_Success)) {
        wprintf(L"NetValidateName was successful\n", nStatus);
    } else {
        wprintf(L"NetValidateName failed with error: %lu (0x%lx)\n", nStatus,
                nStatus);
        wprintf(L"   Error = ");
        switch (nStatus) {
        case ERROR_INVALID_PARAMETER:
            wprintf(L"ERROR_INVALID_PARAMETER\n");
            break;
        case ERROR_DUP_NAME:
            wprintf(L"ERROR_DUP_NAME\n");
            break;
        case ERROR_NO_SUCH_DOMAIN:
            wprintf(L"ERROR_NO_SUCH_DOMAIN\n");
            break;
        case ERROR_NOT_SUPPORTED:
            wprintf(L"ERROR_NOT_SUPPORTED\n");
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
        case NERR_InvalidComputer:
            wprintf(L"NERR_InvalidComputer\n");
            break;
        case NERR_InvalidWorkgroupName:
            wprintf(L"NERR_InvalidWorkgroupName\n");
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

<a href="/windows/desktop/NetMgmt/directory-service-functions">Directory Service Functions</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netgetjoininformation">NetGetJoinInformation</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netgetjoinableous">NetGetJoinableOUs</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain">NetJoinDomain</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netrenamemachineindomain">NetRenameMachineInDomain</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netunjoindomain">NetUnjoinDomain</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>