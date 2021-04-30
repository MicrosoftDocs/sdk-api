---
UID: NF:lmshare.NetSessionGetInfo
title: NetSessionGetInfo function (lmshare.h)
description: Retrieves information about a session established between a particular server and workstation.
helpviewer_keywords: ["0","1","10","2","NetSessionGetInfo","NetSessionGetInfo function [Files]","_win32_netsessiongetinfo","fs.netsessiongetinfo","lmshare/NetSessionGetInfo","netmgmt.netsessiongetinfo"]
old-location: fs\netsessiongetinfo.htm
tech.root: fs
ms.assetid: d44fb8d8-2b64-4268-8603-7784e2c5f2d5
ms.date: 12/05/2018
ms.keywords: 0, 1, 10, 2, NetSessionGetInfo, NetSessionGetInfo function [Files], _win32_netsessiongetinfo, fs.netsessiongetinfo, lmshare/NetSessionGetInfo, netmgmt.netsessiongetinfo
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
 - NetSessionGetInfo
 - lmshare/NetSessionGetInfo
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
 - NetSessionGetInfo
---

# NetSessionGetInfo function


## -description

Retrieves information about a session established between a particular server and workstation.

## -parameters

### -param servername [in]

Pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param UncClientName [in]

Pointer to a string that specifies the name of the computer session for which information is to be returned. This parameter is required and cannot be <b>NULL</b>. For more information, see 
<a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum">NetSessionEnum</a>.

### -param username [in]

Pointer to a string that specifies the name of the user whose session information is to be returned. This parameter is required and cannot be <b>NULL</b>.

### -param level [in]

Specifies the information level of the data. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
Return the name of the computer that established the session. 


The <i>bufptr</i> parameter points to a 
<a href="/windows/desktop/api/lmshare/ns-lmshare-session_info_0">SESSION_INFO_0</a> structure.
							

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Return the name of the computer, name of the user, and open files, pipes, and devices on the computer. 


The <i>bufptr</i> parameter points to a 
<a href="/windows/desktop/api/lmshare/ns-lmshare-session_info_1">SESSION_INFO_1</a> structure.
							

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
In addition to the information indicated for level 1, return the type of client and how the user established the session. 


The <i>bufptr</i> parameter points to a 
<a href="/windows/desktop/api/lmshare/ns-lmshare-session_info_2">SESSION_INFO_2</a> structure.
							

</td>
</tr>
<tr>
<td width="40%"><a id="10"></a><dl>
<dt><b>10</b></dt>
</dl>
</td>
<td width="60%">
Return the name of the computer; name of the user; and active and idle times for the session. 


The <i>bufptr</i> parameter points to a 
<a href="/windows/desktop/api/lmshare/ns-lmshare-session_info_10">SESSION_INFO_10</a> structure.
							

</td>
</tr>
</table>

### -param bufptr [out]

Pointer to the buffer that receives the data. The format of this data depends on the value of the <i>level</i> parameter. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a> and 
<a href="/windows/desktop/NetMgmt/network-management-function-buffer-lengths">Network Management Function Buffer Lengths</a>. 




This buffer is allocated by the system and must be freed using the 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function.

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
<dt><b>ERROR_INVALID_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
The value specified for the <i>level</i> parameter is not valid.

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
A session does not exist with the computer name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_InvalidComputer</b></dt>
</dl>
</td>
<td width="60%">
The computer name is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_UserNotFound</b></dt>
</dl>
</td>
<td width="60%">
The user name could not be found.

</td>
</tr>
</table>

## -remarks

Only members of the Administrators or Server Operators local group can successfully execute the 
<b>NetSessionGetInfo</b> function at level 1 or level 2. No special group membership is required for level 0 or level 10 calls.

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management session functions. For more information, see 
<a href="/windows/desktop/api/iads/nn-iads-iadssession">IADsSession</a> and 
<a href="/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations">IADsFileServiceOperations</a>.

If you call this function at information level 1 or 2 on a member server or workstation, all authenticated users can view the information.


#### Examples

The following code sample demonstrates how to retrieve information about a session using a call to the 
<b>NetSessionGetInfo</b> function. The sample calls 
<b>NetSessionGetInfo</b>, specifying information level 10 (
<a href="/windows/desktop/api/lmshare/ns-lmshare-session_info_10">SESSION_INFO_10</a>). If the call succeeds, the code prints information about the session. Finally, the sample frees the memory allocated for the information buffer.


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
   DWORD dwLevel = 10;
   LPSESSION_INFO_10 pBuf = NULL;
   LPTSTR pszServerName = NULL;
   LPTSTR pszUNCClientName = NULL;
   LPTSTR pszUserName = NULL;
   NET_API_STATUS nStatus;
   //
   // Check command line arguments.
   //
   if (argc == 3)
   {
      pszUNCClientName = argv[1];
      pszUserName = argv[2];
   }
   else if (argc == 4)
   {
      pszServerName = argv[1];
      pszUNCClientName = argv[2];
      pszUserName = argv[3];
   }
   else
   {
      wprintf(L"Usage: %s [\\\\ServerName] \\\\ClientName UserName\n", argv[0]);
      exit(1);
   }
   //
   // Call the NetSessionGetInfo function, specifying level 10.
   //
   nStatus = NetSessionGetInfo(pszServerName,
                               pszUNCClientName,
                               pszUserName,
                               dwLevel,
                               (LPBYTE *)&pBuf);
   //
   // If the call succeeds,
   //
   if (nStatus == NERR_Success)
   {
      if (pBuf != NULL)
      {
         //
         // Print the session information. 
         //
         wprintf(L"\n\tClient: %s\n", pBuf->sesi10_cname);
         wprintf(L"\tUser:   %s\n", pBuf->sesi10_username);
         printf("\tActive: %d\n", pBuf->sesi10_time);
         printf("\tIdle:   %d\n", pBuf->sesi10_idle_time);
      }
   }
   //
   // Otherwise, indicate a system error.
   //
   else
      fprintf(stderr, "A system error has occurred: %d\n", nStatus);
   //
   // Free the allocated memory.
   //
   if (pBuf != NULL)
      NetApiBufferFree(pBuf);

   return 0;
}

```

## -see-also

<a href="/windows/desktop/api/lmshare/nf-lmshare-netsessiondel">NetSessionDel</a>



<a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum">NetSessionEnum</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-session_info_0">SESSION_INFO_0</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-session_info_1">SESSION_INFO_1</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-session_info_10">SESSION_INFO_10</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-session_info_2">SESSION_INFO_2</a>



<a href="/windows/desktop/NetShare/session-functions">Session
		  Functions</a>