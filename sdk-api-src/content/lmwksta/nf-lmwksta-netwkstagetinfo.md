---
UID: NF:lmwksta.NetWkstaGetInfo
title: NetWkstaGetInfo function
author: windows-sdk-content
description: The NetWkstaGetInfo function returns information about the configuration of a workstation.
old-location: netmgmt\netwkstagetinfo.htm
old-project: NetMgmt
ms.assetid: 08777069-1afd-4482-8090-c65ef0bec1ea
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 100, 101, 102, NetWkstaGetInfo, NetWkstaGetInfo function [Network Management], _win32_netwkstagetinfo, lmwksta/NetWkstaGetInfo, netmgmt.netwkstagetinfo
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: USE_INFO_3, *PUSE_INFO_3, *LPUSE_INFO_3
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetWkstaGetInfo
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# NetWkstaGetInfo function


## -description


The
				<b>NetWkstaGetInfo</b> function returns information about the configuration of a workstation.


## -parameters




### -param OPTIONAL

TBD


### -param level [in]

Specifies the information level of the data. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="100"></a><dl>
<dt><b>100</b></dt>
</dl>
</td>
<td width="60%">
Return information about the workstation environment, including platform-specific information, the name of the domain and the local computer, and information concerning the operating system. The <i>bufptr</i> parameter points to a 
<a href="https://msdn.microsoft.com/c705dadd-cf55-44d9-bf36-09e078112479">WKSTA_INFO_100</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="101"></a><dl>
<dt><b>101</b></dt>
</dl>
</td>
<td width="60%">
In addition to level 100 information, return the path to the LANMAN directory. The <i>bufptr</i> parameter points to a 
<a href="https://msdn.microsoft.com/2b692d40-6229-45ef-9ec6-ee464bba0696">WKSTA_INFO_101</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="102"></a><dl>
<dt><b>102</b></dt>
</dl>
</td>
<td width="60%">
In addition to level 101 information, return the number of users who are logged on to the local computer. The <i>bufptr</i> parameter points to a 
<a href="https://msdn.microsoft.com/01607fb5-c433-439c-aaaa-3736697f7c07">WKSTA_INFO_102</a> structure.

</td>
</tr>
</table>
 


### -param bufptr [out]

Pointer to the buffer that receives the data. The format of this data depends on the value of the <i>level</i> parameter. This buffer is allocated by the system and must be freed using the 
<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a> function. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a> and 
<a href="https://msdn.microsoft.com/08599966-68a1-420b-bbc7-6daac833d08f">Network Management Function Buffer Lengths</a>.


#### - servername [in]

Pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.


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
<dt><b>ERROR_INVALID_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
The <i>level</i> parameter is invalid.

</td>
</tr>
</table>
 




## -remarks



<b>Windows Server 2003 and Windows XP:  </b> If you call this function on a domain controller that is running Active Directory, access is allowed or denied based on the ACL for the securable object. To enable anonymous access, the user Anonymous must be a member of the "Pre-Windows 2000 compatible access" group. This is because anonymous tokens do not include the Everyone group SID by default. If you call this function on a member server or workstation, all authenticated users can view the information. Anonymous access is also permitted if the EveryoneIncludesAnonymous policy setting allows anonymous access. Anonymous access is always permitted for level 100. If you call this function at level 101, authenticated users can view the information. Members of the Administrators, and the Server, System and Print Operator local groups can view information at levels 102 and 502. For more information about restricting anonymous access, see 
<a href="https://msdn.microsoft.com/846a5b81-d5bf-4275-a898-38e6ba308b8f">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="https://msdn.microsoft.com/fd3b718a-5eff-4894-9fc6-d157ddb67330">Access Control Model</a>.

<b>Windows 2000:  </b>If you call this function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the securable object. The default ACL permits all authenticated users and members of the "
<a href="https://docs.microsoft.com/windows/desktop//SecAuthZ/allowing-anonymous-access">Pre-Windows 2000 compatible access</a>" group to view the information. By default, the "Pre-Windows 2000 compatible access" group includes Everyone as a member. This enables anonymous access to the information if the system allows anonymous access. If you call this function on a member server or workstation, all authenticated users can view the information. Anonymous access is also permitted if the RestrictAnonymous policy setting allows anonymous access.

To compile an application that uses this function, define the _WIN32_WINNT macro as 0x0400 or later. For more information,see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.


#### Examples

The following code sample demonstrates how to retrieve information about the configuration elements for a workstation using a call to the 
<b>NetWkstaGetInfo</b> function. The sample calls 
<b>NetWkstaGetInfo</b>, specifying information level 102 (
<a href="https://msdn.microsoft.com/01607fb5-c433-439c-aaaa-3736697f7c07">WKSTA_INFO_102</a>). If the call succeeds, the sample prints information about the workstation. Finally, the code sample frees the memory allocated for the information buffer.

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
#include &lt;windows.h&gt; 
#include &lt;lm.h&gt;

int wmain(int argc, wchar_t *argv[])
{
   DWORD dwLevel = 102;
   LPWKSTA_INFO_102 pBuf = NULL;
   NET_API_STATUS nStatus;
   LPWSTR pszServerName = NULL;
   //
   // Check command line arguments.
   //
   if (argc &gt; 2)
   {
      fwprintf(stderr, L"Usage: %s [\\\\ServerName]\n", argv[0]);
      exit(1);
   }
   // The server is not the default local computer.
   //
   if (argc == 2)
      pszServerName = argv[1];
   //
   // Call the NetWkstaGetInfo function, specifying level 102.
   //
   nStatus = NetWkstaGetInfo(pszServerName,
                             dwLevel,
                             (LPBYTE *)&amp;pBuf);
   //
   // If the call is successful,
   //  print the workstation data.
   //
   if (nStatus == NERR_Success)
   {
      printf("\n\tPlatform: %d\n", pBuf-&gt;wki102_platform_id);
      wprintf(L"\tName:     %s\n", pBuf-&gt;wki102_computername);
      printf("\tVersion:  %d.%d\n", pBuf-&gt;wki102_ver_major,
                                  pBuf-&gt;wki102_ver_minor);
      wprintf(L"\tDomain:   %s\n", pBuf-&gt;wki102_langroup);
      wprintf(L"\tLan Root: %s\n", pBuf-&gt;wki102_lanroot);
      wprintf(L"\t# Logged On Users: %d\n", pBuf-&gt;wki102_logged_on_users);
   }
   //
   // Otherwise, indicate the system error.
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/d746b6c9-5ef1-4174-a84f-44e4e50200cd">NetWkstaSetInfo</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/c705dadd-cf55-44d9-bf36-09e078112479">WKSTA_INFO_100</a>



<a href="https://msdn.microsoft.com/2b692d40-6229-45ef-9ec6-ee464bba0696">WKSTA_INFO_101</a>



<a href="https://msdn.microsoft.com/01607fb5-c433-439c-aaaa-3736697f7c07">WKSTA_INFO_102</a>



<a href="https://msdn.microsoft.com/cc400f43-297b-4ff4-8353-b268839c48b8">Workstation and Workstation User Functions</a>
 

 

