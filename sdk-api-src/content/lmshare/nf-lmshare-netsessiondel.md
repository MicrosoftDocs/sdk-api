---
UID: NF:lmshare.NetSessionDel
title: NetSessionDel function (lmshare.h)
description: Ends a network session between a server and a workstation.
helpviewer_keywords: ["NetSessionDel","NetSessionDel function [Files]","_win32_netsessiondel","fs.netsessiondel","lmshare/NetSessionDel","netmgmt.netsessiondel"]
old-location: fs\netsessiondel.htm
tech.root: fs
ms.assetid: a1360f5d-9fd0-44af-b9f5-ab9bc057dfe6
ms.date: 12/05/2018
ms.keywords: NetSessionDel, NetSessionDel function [Files], _win32_netsessiondel, fs.netsessiondel, lmshare/NetSessionDel, netmgmt.netsessiondel
req.header: lmshare.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - NetSessionDel
 - lmshare/NetSessionDel
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
 - NetSessionDel
---

# NetSessionDel function


## -description

Ends a network session between a server and a workstation.

## -parameters

### -param servername [in]

Pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param UncClientName [in]

Pointer to a string that specifies the computer name of the client to disconnect. If the <i>UncClientName</i> parameter is <b>NULL</b>, then all the sessions of the user identified by the <i>username</i> parameter will be deleted on the server specified by the <i>servername</i> parameter. For more information, see 
<a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum">NetSessionEnum</a>.

### -param username [in]

Pointer to a string that specifies the name of the user whose session is to be terminated. If this parameter is <b>NULL</b>, all users' sessions from the client specified by the <i>UncClientName</i> parameter are to be terminated.

## -returns

If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value can be one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The user does not have access to the requested information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The specified parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory is available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_ClientNameNotFound</b></dt>
</dl>
</td>
<td width="60%">
A session does not exist with that computer name.

</td>
</tr>
</table>

## -remarks

Only members of the Administrators or Server Operators local group can successfully execute the 
<b>NetSessionDel</b> function.

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management session functions. For more information, see 
<a href="/windows/desktop/api/iads/nn-iads-iadssession">IADsSession</a> and 
<a href="/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations">IADsFileServiceOperations</a>.


#### Examples

The following code sample demonstrates how to terminate a session between a server and a workstation using a call to the <b>NetSessionDel</b> function.


```cpp
#ifndef UNICODE
#define UNICODE
#endif
#pragma comment(lib, "Netapi32.lib")

#include <stdio.h>
#include <windows.h> 
#include <lm.h>

int wmain(int argc, wchar_t *argv[])
{
   DWORD dwError = 0;
   LPTSTR pszServerName = NULL;
   LPTSTR pszClientName = NULL;
   LPTSTR pszUserName = NULL;
   NET_API_STATUS nStatus;
   //
   // Check command line arguments.
   //
   if (argc > 4)
   {
      wprintf(L"Usage: %s [\\\\ServerName] [\\\\ClientName] [UserName]\n", argv[0]);
      exit(1);
   }

   if (argc >= 2)
      pszServerName = argv[1];

   if (argc >= 3)
      pszClientName = argv[2];

   if (argc == 4)
      pszUserName = argv[3];
   //
   // Call the NetSessionDel function to delete the session.
   //
   nStatus = NetSessionDel(pszServerName,
                           pszClientName,
                           pszUserName);
   //
   // Display the result of the call.
   //
   if (nStatus == NERR_Success)
      fprintf(stderr, "The specified session(s) has been successfully deleted\n");
   else
      fprintf(stderr, "A system error has occurred: %d\n", nStatus);

   return 0;
}

```

## -see-also

<a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum">NetSessionEnum</a>



<a href="/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo">NetSessionGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/NetShare/session-functions">Session
		  Functions</a>