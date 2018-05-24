---
UID: NF:lmaccess.NetUserAdd
title: NetUserAdd function
author: windows-driver-content
description: The NetUserAdd function adds a user account and assigns a password and privilege level.
old-location: netmgmt\netuseradd.htm
old-project: NetMgmt
ms.assetid: b5ca5f76-d40b-4abf-925a-0de54fc476e4
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: 1, 2, 3, 4, NetUserAdd, NetUserAdd function [Network Management], _win32_netuseradd, lmaccess/NetUserAdd, netmgmt.netuseradd
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
req.typenames: MSA_INFO_STATE, *PMSA_INFO_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Netapi32.dll
api_name:
-	NetUserAdd
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# NetUserAdd function


## -description


The
				<b>NetUserAdd</b> function adds a user account and assigns a password and privilege level.


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
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Specifies information about the user account. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/f17a1aef-45f1-461f-975d-75221d08277c">USER_INFO_1</a> structure. 




When you specify this level, the call initializes certain attributes to their default values. For more information, see the following Remarks section.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Specifies level one information and additional attributes about the user account. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/50c78c6a-a08f-473b-929a-9528e618165f">USER_INFO_2</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
Specifies level two information and additional attributes about the user account. This level is valid only on servers. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/39ed05f5-165d-4cb8-98af-e4120a1634f6">USER_INFO_3</a> structure. Note that  it is recommended that you use 
<a href="https://msdn.microsoft.com/66b11a5f-1c2d-4564-8845-9e2fa1f40f3e">USER_INFO_4</a> instead.

</td>
</tr>
<tr>
<td width="40%"><a id="4"></a><dl>
<dt><b>4</b></dt>
</dl>
</td>
<td width="60%">
 Specifies level two information and additional attributes about the user account. This level is valid only on servers. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/66b11a5f-1c2d-4564-8845-9e2fa1f40f3e">USER_INFO_4</a> structure.

<b>Windows 2000:  </b>This level is not supported.

</td>
</tr>
</table>
 


### -param buf [in]

Pointer to the buffer that specifies the data. The format of this data depends on the value of the <i>level</i> parameter. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a>.


#### - parm_err [out]

Pointer to a value that receives the index of the first member of the user information structure that causes ERROR_INVALID_PARAMETER. If this parameter is <b>NULL</b>, the index is not returned on error. For more information, see the 
<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a> function.


#### - servername [in]

Pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used. 




This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.


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
<dt><b>NERR_GroupExists</b></dt>
</dl>
</td>
<td width="60%">
The group already exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_UserExists</b></dt>
</dl>
</td>
<td width="60%">
The user account already exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_PasswordTooShort</b></dt>
</dl>
</td>
<td width="60%">
The password is shorter than required. (The password could also be too long, be too recent in its change history, not have enough unique characters, or not meet another password policy requirement.)

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

The security descriptor of the user container is used to perform the access check for this function. The caller must be able to create child objects of the user class.

Server users must use a system in which the server creates a system account for the new user. The creation of this account is controlled by several parameters in the server's LanMan.ini file.

If the newly added user already exists as a system user, the <b>usri1_home_dir</b> member of the 
<a href="https://msdn.microsoft.com/f17a1aef-45f1-461f-975d-75221d08277c">USER_INFO_1</a> structure is ignored.

When you call the 
<b>NetUserAdd</b> function and specify information level 1, the call initializes the additional members in the 
<a href="https://msdn.microsoft.com/50c78c6a-a08f-473b-929a-9528e618165f">USER_INFO_2</a>, 
<a href="https://msdn.microsoft.com/39ed05f5-165d-4cb8-98af-e4120a1634f6">USER_INFO_3</a>, and 
<a href="https://msdn.microsoft.com/66b11a5f-1c2d-4564-8845-9e2fa1f40f3e">USER_INFO_4</a> structures to their default values. You can change the default values by making subsequent calls to the 
<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a> function. The default values supplied are listed following. (The prefix usriX indicates that the member can begin with multiple prefixes, for example, usri2_ or usri4_.)

<table>
<tr>
<th>Member</th>
<th>Default Value</th>
</tr>
<tr>
<td>usriX_auth_flags</td>
<td>None (0)</td>
</tr>
<tr>
<td>usriX_full_name</td>
<td>None (null string)</td>
</tr>
<tr>
<td>usriX_usr_comment</td>
<td>None (null string)</td>
</tr>
<tr>
<td>usriX_parms</td>
<td>None (null string)</td>
</tr>
<tr>
<td>usriX_workstations</td>
<td>All (null string)</td>
</tr>
<tr>
<td>usriX_acct_expires</td>
<td>Never (TIMEQ_FOREVER)</td>
</tr>
<tr>
<td>usriX_max_storage</td>
<td>Unlimited (USER_MAXSTORAGE_UNLIMITED)</td>
</tr>
<tr>
<td>usriX_logon_hours</td>
<td>Logon allowed at any time (each element 0xFF; all bits set to 1)</td>
</tr>
<tr>
<td>usriX_logon_server</td>
<td>Any domain controller (\\*)</td>
</tr>
<tr>
<td>usriX_country_code</td>
<td>0</td>
</tr>
<tr>
<td>usriX_code_page</td>
<td>0</td>
</tr>
</table>
 

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.


#### Examples

The following code sample demonstrates how to add a user account and assign a privilege level using a call to the 
<b>NetUserAdd</b> function. The code sample fills in the members of the 
<a href="https://msdn.microsoft.com/f17a1aef-45f1-461f-975d-75221d08277c">USER_INFO_1</a> structure and calls 
<b>NetUserAdd</b>, specifying information level 1.

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
   USER_INFO_1 ui;
   DWORD dwLevel = 1;
   DWORD dwError = 0;
   NET_API_STATUS nStatus;

   if (argc != 3)
   {
      fwprintf(stderr, L"Usage: %s \\\\ServerName UserName\n", argv[0]);
      exit(1);
   }
   //
   // Set up the USER_INFO_1 structure.
   //  USER_PRIV_USER: name identifies a user, 
   //    rather than an administrator or a guest.
   //  UF_SCRIPT: required 
   //
   ui.usri1_name = argv[2];
   ui.usri1_password = argv[2];
   ui.usri1_priv = USER_PRIV_USER;
   ui.usri1_home_dir = NULL;
   ui.usri1_comment = NULL;
   ui.usri1_flags = UF_SCRIPT;
   ui.usri1_script_path = NULL;
   //
   // Call the NetUserAdd function, specifying level 1.
   //
   nStatus = NetUserAdd(argv[1],
                        dwLevel,
                        (LPBYTE)&amp;ui,
                        &amp;dwError);
   //
   // If the call succeeds, inform the user.
   //
   if (nStatus == NERR_Success)
      fwprintf(stderr, L"User %s has been successfully added on %s\n",
               argv[2], argv[1]);
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




<a href="https://msdn.microsoft.com/c1429b82-4fd1-48b6-8957-04dee0426077">NetUserDel</a>



<a href="https://msdn.microsoft.com/b26ef3c0-934a-4840-8c06-4eaff5c9ff86">NetUserEnum</a>



<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/f17a1aef-45f1-461f-975d-75221d08277c">USER_INFO_1</a>



<a href="https://msdn.microsoft.com/50c78c6a-a08f-473b-929a-9528e618165f">USER_INFO_2</a>



<a href="https://msdn.microsoft.com/66b11a5f-1c2d-4564-8845-9e2fa1f40f3e">USER_INFO_4</a>



<a href="https://msdn.microsoft.com/cf0e5102-3924-46c0-8124-0aa04e95f48d">User Functions</a>
 

 

