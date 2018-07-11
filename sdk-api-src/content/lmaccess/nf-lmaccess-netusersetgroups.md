---
UID: NF:lmaccess.NetUserSetGroups
title: NetUserSetGroups function
author: windows-sdk-content
description: The NetUserSetGroups function sets global group memberships for a specified user account.
old-location: netmgmt\netusersetgroups.htm
old-project: netmgmt
ms.assetid: 7042c43a-09d1-4179-8074-eb055dc279a6
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: 0, 1, NetUserSetGroups, NetUserSetGroups function [Network Management], _win32_netusersetgroups, lmaccess/NetUserSetGroups, netmgmt.netusersetgroups
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MSA_INFO_STATE, *PMSA_INFO_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetUserSetGroups
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# NetUserSetGroups function


## -description


The
				<b>NetUserSetGroups</b> function sets global group memberships for a specified user account.


## -parameters




### -param OPTIONAL

TBD


### -param username [in]

A pointer to a constant string that specifies the name of the user for which to set global group memberships. For more information, see the Remarks section.


### -param level [in]

The information level of the data. This parameter can be one of the following values. 



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
The <i>buf</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/cc0e5d27-91f1-4640-bb80-e73899fabba9">GROUP_USERS_INFO_0</a> structures that specifies global group names.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
The <i>buf</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/d92e7c18-f2c7-4ea5-8bb6-fec023272dbb">GROUP_USERS_INFO_1</a> structures that specifies global group names with attributes.

</td>
</tr>
</table>
 


### -param buf [in]

A pointer to the buffer that specifies the data. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a>.


### -param num_entries [in]

The number of entries contained in the array pointed to by the <i>buf</i> parameter.


#### - servername [in]

A pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used. 



					


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
The system call level is not correct. This error is returned if the <i>level</i> parameter was specified as a value other than 0 or 1. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter passed was not valid. This error is returned if the <i>num_entries</i> parameter was not valid. 

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
<dt><b>NERR_InvalidComputer</b></dt>
</dl>
</td>
<td width="60%">
The computer name is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_NotPrimary</b></dt>
</dl>
</td>
<td width="60%">
The operation is allowed only on the primary domain controller of the domain.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_GroupNotFound</b></dt>
</dl>
</td>
<td width="60%">
The group group name specified by the <b>grui0_name</b> in the <a href="https://msdn.microsoft.com/cc0e5d27-91f1-4640-bb80-e73899fabba9">GROUP_USERS_INFO_0</a> structure or <b>grui1_name</b> member in the <a href="https://msdn.microsoft.com/d92e7c18-f2c7-4ea5-8bb6-fec023272dbb">GROUP_USERS_INFO_1</a> structure pointed to by the <i>buf</i> parameter does not exist.

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
The user name could not be found.

</td>
</tr>
</table>
 




## -remarks



If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management user functions. For more information, see 
<a href="https://msdn.microsoft.com/6eea74c2-2d6d-4dfd-9a22-3da2d5ce49bf">IADsUser</a> and 
<a href="https://msdn.microsoft.com/e2b90a98-5777-42c2-95dd-4623e738c4da">IADsComputer</a>.

If you call this function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the <a href="https://msdn.microsoft.com/32f2ec06-822f-4d1e-bf51-5ae1d7355e60">securable object</a>. The default ACL permits only Domain Admins and Account Operators to call this function. On a member server or workstation, only Administrators and Power Users can call this function. For more information, see 
<a href="https://msdn.microsoft.com/846a5b81-d5bf-4275-a898-38e6ba308b8f">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="https://msdn.microsoft.com/fd3b718a-5eff-4894-9fc6-d157ddb67330">Access Control Model</a>.

The security descriptor of the User object is used to perform the access check for this function.

To grant a user membership in one existing global group, you can call the 
<a href="https://msdn.microsoft.com/a2eefde8-29e3-4fa1-87db-c7f6d24b699d">NetGroupAddUser</a> function.

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.


#### Examples

The following code sample demonstrates how to set global group memberships for a user account with a call to the 
<b>NetUserSetGroups</b> function. The code sample fills in the <b>grui0_name</b> member of the 
<a href="https://msdn.microsoft.com/cc0e5d27-91f1-4640-bb80-e73899fabba9">GROUP_USERS_INFO_0</a> structure and calls 
<b>NetUserSetGroups</b>, specifying information level 0.

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
   DWORD dwLevel = 0;
   GROUP_USERS_INFO_0 gi;
   NET_API_STATUS nStatus;

   if (argc != 4)
   {
      fwprintf(stderr, L"Usage: %s \\\\ServerName UserName GroupName\n", argv[0]);
      exit(1);
   }
   //
   // Fill in the GROUP_USERS_INFO_0 structure member.
   //
   gi.grui0_name = argv[3];
   //
   // Call the NetUserSetGroups function; specify level 0.
   //
   nStatus = NetUserSetGroups(argv[1],
                              argv[2],
                              dwLevel,
                              (LPBYTE)&amp;gi,
                              1);
   //
   // If the call succeeds, inform the user.
   //
   if (nStatus == NERR_Success)
      fwprintf(stderr, L"Group membership has been successful for %s\n", argv[2]);
   //
   // Otherwise, print the system error.
   //
   else
      fprintf(stderr, "A system error has occurred: %d\n", nStatus);

   return 0;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/cc0e5d27-91f1-4640-bb80-e73899fabba9">GROUP_USERS_INFO_0</a>



<a href="https://msdn.microsoft.com/d92e7c18-f2c7-4ea5-8bb6-fec023272dbb">GROUP_USERS_INFO_1</a>



<a href="https://msdn.microsoft.com/a2eefde8-29e3-4fa1-87db-c7f6d24b699d">NetGroupAddUser</a>



<a href="https://msdn.microsoft.com/ecf1a94c-5dda-4f49-81bd-93e551e089f1">NetUserGetGroups</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/cf0e5102-3924-46c0-8124-0aa04e95f48d">User Functions</a>
 

 

