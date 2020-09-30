---
UID: NF:lmaccess.NetUserChangePassword
title: NetUserChangePassword function (lmaccess.h)
description: The NetUserChangePassword function changes a user's password for a specified network server or domain.
helpviewer_keywords: ["NetUserChangePassword","NetUserChangePassword function [Network Management]","_win32_netuserchangepassword","lmaccess/NetUserChangePassword","netmgmt.netuserchangepassword"]
old-location: netmgmt\netuserchangepassword.htm
tech.root: NetMgmt
ms.assetid: e3791756-3bd4-490b-983a-9687373d846b
ms.date: 12/05/2018
ms.keywords: NetUserChangePassword, NetUserChangePassword function [Network Management], _win32_netuserchangepassword, lmaccess/NetUserChangePassword, netmgmt.netuserchangepassword
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
 - NetUserChangePassword
 - lmaccess/NetUserChangePassword
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
 - NetUserChangePassword
---

# NetUserChangePassword function


## -description

The 
				<b>NetUserChangePassword</b> function changes a user's password for a specified network server or domain.

## -parameters

### -param domainname [in]

A pointer to a constant string that specifies the DNS or NetBIOS name of a remote server or domain on which the function is to execute. If this parameter is <b>NULL</b>, the logon domain of the caller is used.

### -param username [in]

A pointer to a constant string that specifies a user name. The 
<b>NetUserChangePassword</b> function changes the password for the specified user.

If this parameter is <b>NULL</b>, the logon name of the caller is used. For more information, see the following Remarks section.

### -param oldpassword [in]

A pointer to a constant string that specifies the user's old password.

### -param newpassword [in]

A pointer to a constant string that specifies the user's new password.

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
<a href="/windows/desktop/api/iads/nn-iads-iadsuser">IADsUser</a> and 
<a href="/windows/desktop/api/iads/nn-iads-iadscomputer">IADsComputer</a>.

If an application calls the <b>NetUserChangePassword</b> function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the <a href="/windows/desktop/SecAuthZ/securable-objects">securable object</a>. The default ACL permits only Domain Admins and Account Operators to call this function. On a member server or workstation, only Administrators and Power Users can call this function. A user can change his or her own password. For more information, see 
<a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="/windows/desktop/SecAuthZ/access-control-model">Access Control Model</a>.

The security descriptor of the User object is used to perform the access check for this function. In addition, the caller must have the "Change password" <a href="/windows/desktop/AD/control-access-rights">control access right</a> on the User object. This right is granted to Anonymous Logon and Everyone by default. 

Note that for the function to succeed, the <i>oldpassword</i> parameter must match the password as it currently exists.

In some cases, the process that calls the 
<b>NetUserChangePassword</b> function must also have the SE_CHANGE_NOTIFY_NAME privilege enabled; otherwise, 
<b>NetUserChangePassword</b> fails and 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_ACCESS_DENIED. This privilege is not required for the 
<a href="/windows/desktop/Services/localsystem-account">LocalSystem account</a> or for accounts that are members of the administrators group. By default, SE_CHANGE_NOTIFY_NAME is enabled for all users, but some administrators may disable the privilege for everyone. For more information about account privileges, see 
<a href="/windows/desktop/SecAuthZ/privileges">Privileges</a> and 
<a href="/windows/desktop/SecAuthZ/authorization-constants">Authorization Constants</a>.

See 
<a href="/windows/desktop/NetMgmt/forcing-a-user-to-change-the-logon-password">Forcing a User to Change the Logon Password</a> for a code sample that demonstrates how to force a user to change the logon password on the next logon using the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusergetinfo">NetUserGetInfo</a> and 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> functions.

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.

The 
<b>NetUserChangePassword</b> function does not control how the <i>oldpassword</i> and <i>newpassword</i> parameters are secured when sent over the network to a remote server. Any encryption of these parameters is handled by the Remote Procedure Call (RPC) mechanism supported by the network redirector that provides the network transport. Encryption is also controlled  by the security mechanisms supported by the local computer and the security mechanisms supported by remote network server or domain specified in the <i>domainname</i>   parameter. For more details on security when the Microsoft network redirector is used and the remote network server is running Microsoft Windows, see the protocol documentation for <a href="/openspecs/windows_protocols/ms-rpce/290c38b1-92fe-4229-91e6-4fc376610c15">MS-RPCE</a>, <a href="/openspecs/windows_protocols/ms-samr/4df07fab-1bbc-452f-8e92-7853a3c7e380">MS-SAMR</a>, <a href="/openspecs/windows_protocols/ms-spng/f377a379-c24f-4a0f-a3eb-0d835389e28a">MS-SPNG</a>, and <a href="/openspecs/windows_protocols/ms-nlmp/b38c36ed-2804-4868-a9ff-8dd3182128e4">MS-NLMP</a>.


#### Examples

The following code sample demonstrates how to change a user's password with a call to the <b>NetUserChangePassword</b> function. All parameters to the function are required.


```cpp
#ifndef UNICODE
#define UNICODE
#endif
#pragma comment(lib, "netapi32.lib")

#include <stdio.h>
#include <windows.h> 
#include <lm.h>

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

```

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusergetinfo">NetUserGetInfo</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/NetMgmt/user-functions">User Functions</a>