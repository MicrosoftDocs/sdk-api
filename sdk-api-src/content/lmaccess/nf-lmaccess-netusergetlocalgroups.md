---
UID: NF:lmaccess.NetUserGetLocalGroups
title: NetUserGetLocalGroups function (lmaccess.h)
description: The NetUserGetLocalGroups function retrieves a list of local groups to which a specified user belongs.
helpviewer_keywords: ["0","NetUserGetLocalGroups","NetUserGetLocalGroups function [Network Management]","_win32_netusergetlocalgroups","lmaccess/NetUserGetLocalGroups","netmgmt.netusergetlocalgroups"]
old-location: netmgmt\netusergetlocalgroups.htm
tech.root: NetMgmt
ms.assetid: cc5c1c15-cad7-4103-a2c9-1a8adf742703
ms.date: 12/05/2018
ms.keywords: 0, NetUserGetLocalGroups, NetUserGetLocalGroups function [Network Management], _win32_netusergetlocalgroups, lmaccess/NetUserGetLocalGroups, netmgmt.netusergetlocalgroups
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
 - NetUserGetLocalGroups
 - lmaccess/NetUserGetLocalGroups
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
 - NetUserGetLocalGroups
---

# NetUserGetLocalGroups function


## -description

The 
				<b>NetUserGetLocalGroups</b> function retrieves a list of local groups to which a specified user belongs.

## -parameters

### -param servername [in]

A pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param username [in]

A pointer to a constant string that specifies the name of the user for which to return local group membership information. If the string is of the form <i>DomainName</i>&#92;<i>UserName</i> the user name is expected to be found on that domain. If the string is of the form <i>UserName</i>, the user name is expected to be found on the server specified by the <i>servername</i> parameter. For more information, see the Remarks section.

### -param level [in]

The information level of the data. This parameter can be the following value. 



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
Return the names of the local groups to which the user belongs. The <i>bufptr</i> parameter points to an array of 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_users_info_0">LOCALGROUP_USERS_INFO_0</a> structures.

</td>
</tr>
</table>

### -param flags [in]

A bitmask of flags that affect the operation. Currently, only the value defined is <b>LG_INCLUDE_INDIRECT</b>. If this bit is set, the function also returns the names of the local groups in which the user is indirectly a member (that is, the user has membership in a global group that is itself a member of one or more local groups).

### -param bufptr [out]

A pointer to the buffer that receives the data. The format of this data depends on the value of the <i>level</i> parameter. This buffer is allocated by the system and must be freed using the 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function. Note that you must free the buffer even if the function fails with <b>ERROR_MORE_DATA</b>.

### -param prefmaxlen [in]

The preferred maximum length, in bytes, of the returned data. If <b>MAX_PREFERRED_LENGTH</b> is specified in this parameter, the function allocates the amount of memory required for the data. If another value is specified in this parameter, it can restrict the number of bytes that the function returns. If the buffer size is insufficient to hold all entries, the function returns <b>ERROR_MORE_DATA</b>. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a> and 
<a href="/windows/desktop/NetMgmt/network-management-function-buffer-lengths">Network Management Function Buffer Lengths</a>.

### -param entriesread [out]

A pointer to a value that receives the count of elements actually enumerated.

### -param totalentries [out]

A pointer to a value that receives the total number of entries that could have been enumerated.

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
The user does not have access rights to the requested information. This error is also returned if the <i>servername</i> parameter has a trailing blank.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
The system call level is not correct. This error is returned if the <i>level</i> parameter was not specified as 0. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is incorrect. This error is returned if the <i>flags</i> parameter contains a value other than <b>LG_INCLUDE_INDIRECT</b>. 

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
<dt><b>NERR_DCNotFound</b></dt>
</dl>
</td>
<td width="60%">
The domain controller could not be found. 

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
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_SERVER_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The RPC server is unavailable. This error is returned if the <i>servername</i> parameter could not be found. 

</td>
</tr>
</table>

## -remarks

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management user functions. For more information, see 
<a href="/windows/desktop/api/iads/nn-iads-iadsuser">IADsUser</a> and 
<a href="/windows/desktop/api/iads/nn-iads-iadscomputer">IADsComputer</a>.

If you call this function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the <a href="/windows/desktop/SecAuthZ/securable-objects">securable object</a>. The default ACL permits all authenticated users and members of the "<a href="/windows/desktop/SecAuthZ/allowing-anonymous-access">Pre-Windows 2000 compatible access</a>" group to view the information. If you call this function on a member server or workstation, all authenticated users can view the information. For  information about anonymous access and restricting anonymous access on these platforms, see 
<a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="/windows/desktop/SecAuthZ/access-control-model">Access Control Model</a>.

The security descriptor of the Domain object is used to perform the access check for this function. The caller must have  Read Property permission on the Domain object.

To retrieve a list of global groups to which a specified user belongs, you can call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusergetgroups">NetUserGetGroups</a> function.

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.


#### Examples

The following code sample demonstrates how to retrieve a list of the local groups to which a user belongs with a call to the 
<b>NetUserGetLocalGroups</b> function. The sample calls 
<b>NetUserGetLocalGroups</b>, specifying information level 0 (<a href="/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_users_info_0">LOCALGROUP_USERS_INFO_0</a>). The sample loops through the entries and prints the name of each local group in which the user has membership. If all available entries are not enumerated, it also prints the number of entries actually enumerated and the total number of entries available. Finally, the code sample frees the memory allocated for the information buffer.


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
   LPLOCALGROUP_USERS_INFO_0 pBuf = NULL;
   DWORD dwLevel = 0;
   DWORD dwFlags = LG_INCLUDE_INDIRECT ;
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
   // Call the NetUserGetLocalGroups function 
   //  specifying information level 0.
   //
   //  The LG_INCLUDE_INDIRECT flag specifies that the 
   //   function should also return the names of the local 
   //   groups in which the user is indirectly a member.
   //
   nStatus = NetUserGetLocalGroups(argv[1],
                                   argv[2],
                                   dwLevel,
                                   dwFlags,
                                   (LPBYTE *) &pBuf,
                                   dwPrefMaxLen,
                                   &dwEntriesRead,
                                   &dwTotalEntries);
   //
   // If the call succeeds,
   //
   if (nStatus == NERR_Success)
   {
      LPLOCALGROUP_USERS_INFO_0 pTmpBuf;
      DWORD i;
      DWORD dwTotalCount = 0;

      if ((pTmpBuf = pBuf) != NULL)
      {
         fprintf(stderr, "\nLocal group(s):\n");
         //
         // Loop through the entries and 
         //  print the names of the local groups 
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

            wprintf(L"\t-- %s\n", pTmpBuf->lgrui0_name);

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
   // Free the allocated memory.
   //
   if (pBuf != NULL)
      NetApiBufferFree(pBuf);

   return 0;
}

```

## -see-also

<a href="/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_users_info_0">LOCALGROUP_USERS_INFO_0</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusergetgroups">NetUserGetGroups</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/NetMgmt/user-functions">User Functions</a>