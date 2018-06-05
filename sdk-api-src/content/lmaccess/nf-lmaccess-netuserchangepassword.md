---
UID: NF:lmaccess.NetUserChangePassword
title: NetUserChangePassword function
author: windows-sdk-content
description: The NetUserChangePassword function changes a user's password for a specified network server or domain.
old-location: netmgmt\netuserchangepassword.htm
old-project: NetMgmt
ms.assetid: e3791756-3bd4-490b-983a-9687373d846b
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: NetUserChangePassword, NetUserChangePassword function [Network Management], _win32_netuserchangepassword, lmaccess/NetUserChangePassword, netmgmt.netuserchangepassword
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
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Netapi32.dll
api_name:
-	NetUserChangePassword
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# NetUserChangePassword function


## -description


The 
				<b>NetUserChangePassword</b> function changes a user's password for a specified network server or domain.


## -parameters




### -param OPTIONAL

TBD


### -param oldpassword [in]

A pointer to a constant string that specifies the user's old password.


### -param newpassword [in]

A pointer to a constant string that specifies the user's new password.


#### - domainname [in]

A pointer to a constant string that specifies the DNS or NetBIOS name of a remote server or domain on which the function is to execute. If this parameter is <b>NULL</b>, the logon domain of the caller is used. 



					


#### - username [in]

A pointer to a constant string that specifies a user name. The 
<b>NetUserChangePassword</b> function changes the password for the specified user.

If this parameter is <b>NULL</b>, the logon name of the caller is used. For more information, see the following Remarks section.


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
<dt><b>ERROR_INVALID_PASSWORD</b></dt>
</dl>
</td>
<td width="60%">
The user has entered an invalid password.

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
<dt><b>NERR_UserNotFound</b></dt>
</dl>
</td>
<td width="60%">
The user name could not be found.

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



If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same result you can achieve by calling the network management user functions. For more information, see 
<a href="https://msdn.microsoft.com/6eea74c2-2d6d-4dfd-9a22-3da2d5ce49bf">IADsUser</a> and 
<a href="https://msdn.microsoft.com/e2b90a98-5777-42c2-95dd-4623e738c4da">IADsComputer</a>.

If an application calls the <b>NetUserChangePassword</b> function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the <a href="https://msdn.microsoft.com/32f2ec06-822f-4d1e-bf51-5ae1d7355e60">securable object</a>. The default ACL permits only Domain Admins and Account Operators to call this function. On a member server or workstation, only Administrators and Power Users can call this function. A user can change his or her own password. For more information, see 
<a href="https://msdn.microsoft.com/846a5b81-d5bf-4275-a898-38e6ba308b8f">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="https://msdn.microsoft.com/fd3b718a-5eff-4894-9fc6-d157ddb67330">Access Control Model</a>.

The security descriptor of the User object is used to perform the access check for this function. In addition, the caller must have the "Change password" <a href="https://msdn.microsoft.com/27ad74bd-ad87-422e-a4a2-02c0d51c4dd4">control access right</a> on the User object. This right is granted to Anonymous Logon and Everyone by default. 

Note that for the function to succeed, the <i>oldpassword</i> parameter must match the password as it currently exists.

In some cases, the process that calls the 
<b>NetUserChangePassword</b> function must also have the SE_CHANGE_NOTIFY_NAME privilege enabled; otherwise, 
<b>NetUserChangePassword</b> fails and 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_ACCESS_DENIED. This privilege is not required for the 
<a href="https://msdn.microsoft.com/692bceb6-f5bd-4b83-ab3b-ef8099dc84e1">LocalSystem account</a> or for accounts that are members of the administrators group. By default, SE_CHANGE_NOTIFY_NAME is enabled for all users, but some administrators may disable the privilege for everyone. For more information about account privileges, see 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff559863">Privileges</a> and 
<a href="https://msdn.microsoft.com/be5637e3-0932-49b6-a5af-a542060545e0">Authorization Constants</a>.

See 
<a href="https://msdn.microsoft.com/828f5d72-3e19-4b65-a1db-ac702fd4cfde">Forcing a User to Change the Logon Password</a> for a code sample that demonstrates how to force a user to change the logon password on the next logon using the 
<a href="https://msdn.microsoft.com/5bd13bed-938a-4273-840e-99fca99f7139">NetUserGetInfo</a> and 
<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a> functions.

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.

The 
<b>NetUserChangePassword</b> function does not control how the <i>oldpassword</i> and <i>newpassword</i> parameters are secured when sent over the network to a remote server. Any encryption of these parameters is handled by the Remote Procedure Call (RPC) mechanism supported by the network redirector that provides the network transport. Encryption is also controlled  by the security mechanisms supported by the local computer and the security mechanisms supported by remote network server or domain specified in the <i>domainname</i>   parameter. For more details on security when the Microsoft network redirector is used and the remote network server is running Microsoft Windows, see the protocol documentation for <a href="http://go.microsoft.com/fwlink/p/?linkid=200126">MS-RPCE</a>, <a href=" http://go.microsoft.com/fwlink/p/?linkid=200128">MS-SAMR</a>, <a href="http://go.microsoft.com/fwlink/p/?linkid=200129">MS-SPNG</a>, and <a href=" http://go.microsoft.com/fwlink/p/?linkid=200130">MS-NLMP</a>.


#### Examples

The following code sample demonstrates how to change a user's password with a call to the <b>NetUserChangePassword</b> function. All parameters to the function are required.

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
   DWORD dwError = 0;
   NET_API_STATUS nStatus;
   //
   // All parameters are required.
   //
   if (argc != 5)
   {
      fwprintf(stderr, L"Usage: %s \\\\ServerName UserName OldPassword NewPassword\n", argv[0]);
      exit(1);
   }
   //
   // Call the NetUserChangePassword function.
   //
   nStatus = NetUserChangePassword(argv[1], argv[2], argv[3], argv[4]);
   //
   // If the call succeeds, inform the user.
   //
   if (nStatus == NERR_Success)
      fwprintf(stderr, L"User password has been changed successfully\n");
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




<a href="https://msdn.microsoft.com/5bd13bed-938a-4273-840e-99fca99f7139">NetUserGetInfo</a>



<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/cf0e5102-3924-46c0-8124-0aa04e95f48d">User Functions</a>
 

 

