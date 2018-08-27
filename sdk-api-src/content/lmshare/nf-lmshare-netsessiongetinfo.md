---
UID: NF:lmshare.NetSessionGetInfo
title: NetSessionGetInfo function
author: windows-sdk-content
description: Retrieves information about a session established between a particular server and workstation.
old-location: fs\netsessiongetinfo.htm
old-project: netshare
ms.assetid: d44fb8d8-2b64-4268-8603-7784e2c5f2d5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 0, 1, 10, 2, NetSessionGetInfo, NetSessionGetInfo function [Files], _win32_netsessiongetinfo, fs.netsessiongetinfo, lmshare/NetSessionGetInfo, netmgmt.netsessiongetinfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: lmshare.h
req.include-header: Lm.h
req.redist: 
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
tech.root: 
req.typenames: SERVER_TRANSPORT_INFO_3, *PSERVER_TRANSPORT_INFO_3, *LPSERVER_TRANSPORT_INFO_3
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetSessionGetInfo
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# NetSessionGetInfo function


## -description


Retrieves information about a session established between a particular server and workstation.


## -parameters




### -param servername [in]

Pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used. 



					


### -param UncClientName [in]

Pointer to a string that specifies the name of the computer session for which information is to be returned. This parameter is required and cannot be <b>NULL</b>. For more information, see 
<a href="https://msdn.microsoft.com/5923a8cc-bf7a-4ffa-b089-fd7f26ee42d2">NetSessionEnum</a>.


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
<a href="https://msdn.microsoft.com/6b39df47-f25c-41dd-ba15-6e6806c4ec89">SESSION_INFO_0</a> structure.
							

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
<a href="https://msdn.microsoft.com/bc1c985e-b8af-4134-9ae4-511d82e3909b">SESSION_INFO_1</a> structure.
							

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
<a href="https://msdn.microsoft.com/c3429eba-4277-4dc7-9255-cd2ff18dc583">SESSION_INFO_2</a> structure.
							

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
<a href="https://msdn.microsoft.com/a23a5647-f99d-4cb8-9d84-93653a3e7428">SESSION_INFO_10</a> structure.
							

</td>
</tr>
</table>
 


### -param bufptr [out]

Pointer to the buffer that receives the data. The format of this data depends on the value of the <i>level</i> parameter. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a> and 
<a href="https://msdn.microsoft.com/08599966-68a1-420b-bbc7-6daac833d08f">Network Management Function Buffer Lengths</a>. 




This buffer is allocated by the system and must be freed using the 
<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a> function.


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
<a href="https://msdn.microsoft.com/54621f0d-7478-4a6f-a96f-f3f93e64b281">IADsSession</a> and 
<a href="https://msdn.microsoft.com/91335658-8efb-4945-9862-f72e78d749d6">IADsFileServiceOperations</a>.

If you call this function at information level 1 or 2 on a member server or workstation, all authenticated users can view the information.


#### Examples

The following code sample demonstrates how to retrieve information about a session using a call to the 
<b>NetSessionGetInfo</b> function. The sample calls 
<b>NetSessionGetInfo</b>, specifying information level 10 (
<a href="https://msdn.microsoft.com/a23a5647-f99d-4cb8-9d84-93653a3e7428">SESSION_INFO_10</a>). If the call succeeds, the code prints information about the session. Finally, the sample frees the memory allocated for the information buffer.


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




<a href="https://msdn.microsoft.com/a1360f5d-9fd0-44af-b9f5-ab9bc057dfe6">NetSessionDel</a>



<a href="https://msdn.microsoft.com/5923a8cc-bf7a-4ffa-b089-fd7f26ee42d2">NetSessionEnum</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/6b39df47-f25c-41dd-ba15-6e6806c4ec89">SESSION_INFO_0</a>



<a href="https://msdn.microsoft.com/bc1c985e-b8af-4134-9ae4-511d82e3909b">SESSION_INFO_1</a>



<a href="https://msdn.microsoft.com/a23a5647-f99d-4cb8-9d84-93653a3e7428">SESSION_INFO_10</a>



<a href="https://msdn.microsoft.com/c3429eba-4277-4dc7-9255-cd2ff18dc583">SESSION_INFO_2</a>



<a href="https://msdn.microsoft.com/931455e3-1301-4a68-93c3-2674b3d4c491">Session
		  Functions</a>
 

 

