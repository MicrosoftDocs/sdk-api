---
UID: NF:lmaccess.NetUserGetGroups
title: NetUserGetGroups function
author: windows-sdk-content
description: The NetUserGetGroups function retrieves a list of global groups to which a specified user belongs.
old-location: netmgmt\netusergetgroups.htm
tech.root: netmgmt
ms.assetid: ecf1a94c-5dda-4f49-81bd-93e551e089f1
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: 0, 1, NetUserGetGroups, NetUserGetGroups function [Network Management], _win32_netusergetgroups, lmaccess/NetUserGetGroups, netmgmt.netusergetgroups
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetUserGetGroups
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NetUserGetGroups function


## -description


The
				<b>NetUserGetGroups</b> function retrieves a list of global groups to which a specified user belongs.


## -parameters




### -param servername [in]

A pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used. 



					


### -param username [in]

A pointer to a constant string that specifies the name of the user to search for in each group account. For more information, see the following Remarks section.


### -param level [in]

The information level of the data requested. This parameter can be one of the following values. 



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
Return the names of the global groups to which the user belongs. The <i>bufptr</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/cc0e5d27-91f1-4640-bb80-e73899fabba9">GROUP_USERS_INFO_0</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Return the names of the global groups to which the user belongs with attributes. The <i>bufptr</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/d92e7c18-f2c7-4ea5-8bb6-fec023272dbb">GROUP_USERS_INFO_1</a> structures.

</td>
</tr>
</table>
 


### -param bufptr [out]

A pointer to the buffer that receives the data. This buffer is allocated by the system and must be freed using the 
<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a> function. Note that you must free the buffer even if the function fails with ERROR_MORE_DATA.


### -param prefmaxlen [in]

The preferred maximum length, in bytes, of returned data. If MAX_PREFERRED_LENGTH is specified, the function allocates the amount of memory required for the data. If another value is specified in this parameter, it can restrict the number of bytes that the function returns. If the buffer size is insufficient to hold all entries, the function returns ERROR_MORE_DATA. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a> and 
<a href="https://msdn.microsoft.com/08599966-68a1-420b-bbc7-6daac833d08f">Network Management Function Buffer Lengths</a>.


### -param entriesread [out]

A pointer to a value that receives the count of elements actually retrieved.


### -param totalentries [out]

A pointer to a value that receives the total number of entries that could have been retrieved.


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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The user does not have access rights to the requested information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_NETPATH</b></dt>
</dl>
</td>
<td width="60%">
The network path was not found. This error is returned if the <i>servername</i> parameter could not be found. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
The system call level is not correct. This error is returned if the <i>level</i> parameter was specified as a value other than 0 or 1. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_NAME</b></dt>
</dl>
</td>
<td width="60%">
The name syntax is incorrect. This error is returned if the <i>servername</i> parameter has leading or trailing blanks or contains an illegal character. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
More entries are available. Specify a large enough buffer to receive all entries.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory was available to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_InternalError</b></dt>
</dl>
</td>
<td width="60%">
An internal error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_UserNotFound</b></dt>
</dl>
</td>
<td width="60%">
The user could not be found. This error is returned if the <i>username</i> could not be found.

</td>
</tr>
</table>
 




## -remarks



If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management user functions. For more information, see 
<a href="https://msdn.microsoft.com/6eea74c2-2d6d-4dfd-9a22-3da2d5ce49bf">IADsUser</a> and 
<a href="https://msdn.microsoft.com/e2b90a98-5777-42c2-95dd-4623e738c4da">IADsComputer</a>.

If you call this function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the <a href="https://msdn.microsoft.com/32f2ec06-822f-4d1e-bf51-5ae1d7355e60">securable object</a>. The default ACL permits all authenticated users and members of the "<a href="https://msdn.microsoft.com/library/Aa375347(v=VS.85).aspx">Pre-Windows 2000 compatible access</a>" group to view the information. If you call this function on a member server or workstation, all authenticated users can view the information. For  information about anonymous access and restricting anonymous access on these platforms, see 
<a href="https://msdn.microsoft.com/846a5b81-d5bf-4275-a898-38e6ba308b8f">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="https://msdn.microsoft.com/fd3b718a-5eff-4894-9fc6-d157ddb67330">Access Control Model</a>.

The security descriptor of the User object is used to perform the access check for this function.

To retrieve a list of the local groups to which a user belongs, you can call the 
<a href="https://msdn.microsoft.com/cc5c1c15-cad7-4103-a2c9-1a8adf742703">NetUserGetLocalGroups</a> function. Network groups are separate and distinct from Windows NT system groups.

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.


#### Examples

The following code sample demonstrates how to retrieve a list of global groups to which a user belongs with a call to the 
<b>NetUserGetGroups</b> function. The sample calls 
<b>NetUserGetGroups</b>, specifying information level 0 (
<a href="https://msdn.microsoft.com/cc0e5d27-91f1-4640-bb80-e73899fabba9">GROUP_USERS_INFO_0</a>). The code loops through the entries and prints the name of the global groups in which the user has membership. The sample also prints the total number of entries that are available and the number of entries actually enumerated if they do not match. Finally, the code sample frees the memory allocated for the buffer.


```cpp
#ifndef UNICODE
#define UNICODE
#endif
#pragma comment(lib, "netapi32.lib")

#include <stdio.h>
#include <assert.h>
#include <windows.h> 
#include <lm.h>

int wmain(int argc, wchar_t *argv[])
{
   LPGROUP_USERS_INFO_0 pBuf = NULL;
   DWORD dwLevel = 0;
   DWORD dwPrefMaxLen = MAX_PREFERRED_LENGTH;
   DWORD dwEntriesRead = 0;
   DWORD dwTotalEntries = 0;
   NET_API_STATUS nStatus;

   if (argc != 3)
   {
      fwprintf(stderr, L"Usage: %s \\\\ServerName UserName\n", argv[0]);
      exit(1);
   }
   //
   // Call the NetUserGetGroups function, specifying level 0.
   //
   nStatus = NetUserGetGroups(argv[1],
                              argv[2],
                              dwLevel,
                              (LPBYTE*)&pBuf,
                              dwPrefMaxLen,
                              &dwEntriesRead,
                              &dwTotalEntries);
   //
   // If the call succeeds,
   //
   if (nStatus == NERR_Success)
   {
      LPGROUP_USERS_INFO_0 pTmpBuf;
      DWORD i;
      DWORD dwTotalCount = 0;

      if ((pTmpBuf = pBuf) != NULL)
      {
         fprintf(stderr, "\nGlobal group(s):\n");
         //
         // Loop through the entries; 
         //  print the name of the global groups 
         //  to which the user belongs.
         //
         for (i = 0; i < dwEntriesRead; i++)
         {
            assert(pTmpBuf != NULL);

            if (pTmpBuf == NULL)
            {
               fprintf(stderr, "An access violation has occurred\n");
               break;
            }

            wprintf(L"\t-- %s\n", pTmpBuf->grui0_name);

            pTmpBuf++;
            dwTotalCount++;
         }
      }
      //
      // If all available entries were
      //  not enumerated, print the number actually 
      //  enumerated and the total number available.
      //
      if (dwEntriesRead < dwTotalEntries)
         fprintf(stderr, "\nTotal entries: %d", dwTotalEntries);
      //
      // Otherwise, just print the total.
      //
      printf("\nEntries enumerated: %d\n", dwTotalCount);
   }
   else
      fprintf(stderr, "A system error has occurred: %d\n", nStatus);
   //
   // Free the allocated buffer.
   //
   if (pBuf != NULL)
      NetApiBufferFree(pBuf);

   return 0;
}

```





## -see-also




<a href="https://msdn.microsoft.com/cc0e5d27-91f1-4640-bb80-e73899fabba9">GROUP_USERS_INFO_0</a>



<a href="https://msdn.microsoft.com/d92e7c18-f2c7-4ea5-8bb6-fec023272dbb">GROUP_USERS_INFO_1</a>



<a href="https://msdn.microsoft.com/a9bcb806-f44c-4db2-9644-06687b31405d">NetGroupGetUsers</a>



<a href="https://msdn.microsoft.com/049f1ea3-4d23-4b35-8b08-7256859aed45">NetQueryDisplayInformation</a>



<a href="https://msdn.microsoft.com/5bd13bed-938a-4273-840e-99fca99f7139">NetUserGetInfo</a>



<a href="https://msdn.microsoft.com/cc5c1c15-cad7-4103-a2c9-1a8adf742703">NetUserGetLocalGroups</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/cf0e5102-3924-46c0-8124-0aa04e95f48d">User Functions</a>
 

 

