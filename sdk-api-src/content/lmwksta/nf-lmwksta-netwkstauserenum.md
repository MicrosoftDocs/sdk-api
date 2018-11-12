---
UID: NF:lmwksta.NetWkstaUserEnum
title: NetWkstaUserEnum function
author: windows-sdk-content
description: The NetWkstaUserEnum function lists information about all users currently logged on to the workstation. This list includes interactive, service and batch logons.
old-location: netmgmt\netwkstauserenum.htm
tech.root: NetMgmt
ms.assetid: 42eaeb70-3ce8-4eae-b20b-4729db90a7ef
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 0, 1, NetWkstaUserEnum, NetWkstaUserEnum function [Network Management], _win32_netwkstauserenum, lmwksta/NetWkstaUserEnum, netmgmt.netwkstauserenum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: lmwksta.h
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
 - NetWkstaUserEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NetWkstaUserEnum function


## -description


The
				<b>NetWkstaUserEnum</b> function lists information about all users currently logged on to the workstation. This list includes interactive, service and batch logons.


## -parameters




### -param servername [in]

Pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.


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
Return the names of users currently logged on to the workstation. The <i>bufptr</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/8bd8d8c7-4558-46cb-ab46-a2197d53e9f7">WKSTA_USER_INFO_0</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Return the names of the current users and the domains accessed by the workstation. The <i>bufptr</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/a30747de-6cb0-41dc-95a7-be3d471056d5">WKSTA_USER_INFO_1</a> structures.

</td>
</tr>
</table>
 


### -param bufptr [out]

Pointer to the buffer that receives the data. The format of this data depends on the value of the <i>level</i> parameter. This buffer is allocated by the system and must be freed using the 
<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a> function. Note that you must free the buffer even if the function fails with ERROR_MORE_DATA.


### -param prefmaxlen [in]

Specifies the preferred maximum length of returned data, in bytes. If you specify MAX_PREFERRED_LENGTH, the function allocates the amount of memory required for the data. If you specify another value in this parameter, it can restrict the number of bytes that the function returns. If the buffer size is insufficient to hold all entries, the function returns ERROR_MORE_DATA. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a> and 
<a href="https://msdn.microsoft.com/08599966-68a1-420b-bbc7-6daac833d08f">Network Management Function Buffer Lengths</a>.


### -param entriesread [out]

Pointer to a value that receives the count of elements actually enumerated.


### -param totalentries [out]

Pointer to a value that receives the total number of entries that could have been enumerated from the current resume position. Note that applications should consider this value only as a hint.


### -param resumehandle [in, out]

Pointer to a value that contains a resume handle which is used to continue an existing search. The handle should be zero on the first call and left unchanged for subsequent calls. If this parameter is <b>NULL</b>, no resume handle is stored.


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
The user does not have access to the requested information.

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
<dt><b>ERROR_INVALID_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
The <i>level</i> parameter is invalid.

</td>
</tr>
</table>
 




## -remarks



Note that since the 
<b>NetWkstaUserEnum</b> function lists entries for service and batch logons, as well as for interactive logons, the function can return entries for users who have logged off a workstation. This can occur, for example, when a user calls a service that impersonates the user. In this instance, 
<b>NetWkstaUserEnum</b> returns an entry for the user until the service stops impersonating the user.

<b>Windows Server 2003 and Windows XP:  </b>If you call this function on a domain controller that is running Active Directory, access is allowed or denied based on the ACL for the securable object. To enable anonymous access, the user Anonymous must be a member of the "Pre-Windows 2000 compatible access" group. This is because anonymous tokens do not include the Everyone group SID by default. If you call this function on a member server or workstation, all authenticated users can view the information. Anonymous access is also permitted if the RestrictAnonymous policy setting permits anonymous access. If the RestrictAnonymous policy setting does not permit anonymous access, only an administrator can successfully execute the function. Members of the Administrators, and the Server, System and Print Operator local groups can also view information. For more information about restricting anonymous access, see 
<a href="https://msdn.microsoft.com/846a5b81-d5bf-4275-a898-38e6ba308b8f">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="https://msdn.microsoft.com/fd3b718a-5eff-4894-9fc6-d157ddb67330">Access Control Model</a>.

<b>Windows 2000:  </b>If you call this function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the securable object. The default ACL permits all authenticated users and members of the "
<a href="security.pre_windows_2000_compatible_access_group">Pre-Windows 2000 compatible access</a>" group to view the information. By default, the "Pre-Windows 2000 compatible access" group includes Everyone as a member. This enables anonymous access to the information if the system allows anonymous access. If you call this function on a member server or workstation, all authenticated users can view the information. Anonymous access is also permitted if the RestrictAnonymous policy setting allows anonymous access.

To compile an application that uses this function, define the _WIN32_WINNT macro as 0x0400 or later. For more information,see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.


#### Examples

The following code sample demonstrates how to list information about all users currently logged on to a workstation using a call to the 
<b>NetWkstaUserEnum</b> function. The sample calls 
<b>NetWkstaUserEnum</b>, specifying information level 0 (
<a href="https://msdn.microsoft.com/8bd8d8c7-4558-46cb-ab46-a2197d53e9f7">WKSTA_USER_INFO_0</a>). The sample loops through the entries and prints the names of the users logged on to a workstation. Finally, the code sample frees the memory allocated for the information buffer, and prints the total number of users enumerated.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#ifndef UNICODE
#define UNICODE
#endif
#pragma comment(lib, "netapi32.lib")

#include &lt;stdio.h&gt;
#include &lt;assert.h&gt;
#include &lt;windows.h&gt; 
#include &lt;lm.h&gt;

int wmain(int argc, wchar_t *argv[])
{
   LPWKSTA_USER_INFO_0 pBuf = NULL;
   LPWKSTA_USER_INFO_0 pTmpBuf;
   DWORD dwLevel = 0;
   DWORD dwPrefMaxLen = MAX_PREFERRED_LENGTH;
   DWORD dwEntriesRead = 0;
   DWORD dwTotalEntries = 0;
   DWORD dwResumeHandle = 0;
   DWORD i;
   DWORD dwTotalCount = 0;
   NET_API_STATUS nStatus;
   LPWSTR pszServerName = NULL;

   if (argc &gt; 2)
   {
      fwprintf(stderr, L"Usage: %s [\\\\ServerName]\n", argv[0]);
      exit(1);
   }
   // The server is not the default local computer.
   //
   if (argc == 2)
      pszServerName = argv[1];
   fwprintf(stderr, L"\nUsers currently logged on %s:\n", pszServerName);
   //
   // Call the NetWkstaUserEnum function, specifying level 0.
   //
   do // begin do
   {
      nStatus = NetWkstaUserEnum( pszServerName,
                                  dwLevel,
                                  (LPBYTE*)&amp;pBuf,
                                  dwPrefMaxLen,
                                  &amp;dwEntriesRead,
                                  &amp;dwTotalEntries,
                                  &amp;dwResumeHandle);
      //
      // If the call succeeds,
      //
      if ((nStatus == NERR_Success) || (nStatus == ERROR_MORE_DATA))
      {
         if ((pTmpBuf = pBuf) != NULL)
         {
            //
            // Loop through the entries.
            //
            for (i = 0; (i &lt; dwEntriesRead); i++)
            {
               assert(pTmpBuf != NULL);

               if (pTmpBuf == NULL)
               {
                  //
                  // Only members of the Administrators local group
                  //  can successfully execute NetWkstaUserEnum
                  //  locally and on a remote server.
                  //
                  fprintf(stderr, "An access violation has occurred\n");
                  break;
               }
               //
               // Print the user logged on to the workstation. 
               //
               wprintf(L"\t-- %s\n", pTmpBuf-&gt;wkui0_username);

               pTmpBuf++;
               dwTotalCount++;
            }
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
      {
         NetApiBufferFree(pBuf);
         pBuf = NULL;
      }
   }
   // 
   // Continue to call NetWkstaUserEnum while 
   //  there are more entries. 
   // 
   while (nStatus == ERROR_MORE_DATA); // end do
   //
   // Check again for allocated memory.
   //
   if (pBuf != NULL)
      NetApiBufferFree(pBuf);
   //
   // Print the final count of workstation users.
   //
   fprintf(stderr, "\nTotal of %d entries enumerated\n", dwTotalCount);

   return 0;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/08777069-1afd-4482-8090-c65ef0bec1ea">NetWkstaGetInfo</a>



<a href="https://msdn.microsoft.com/d746b6c9-5ef1-4174-a84f-44e4e50200cd">NetWkstaSetInfo</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/8bd8d8c7-4558-46cb-ab46-a2197d53e9f7">WKSTA_USER_INFO_0</a>



<a href="https://msdn.microsoft.com/a30747de-6cb0-41dc-95a7-be3d471056d5">WKSTA_USER_INFO_1</a>



<a href="https://msdn.microsoft.com/cc400f43-297b-4ff4-8353-b268839c48b8">Workstation and Workstation User Functions</a>
 

 

