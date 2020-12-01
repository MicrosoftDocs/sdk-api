---
UID: NF:lmaccess.NetUserModalsSet
title: NetUserModalsSet function (lmaccess.h)
description: The NetUserModalsSet function sets global information for all users and global groups in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.
helpviewer_keywords: ["0","1","1001","1002","1003","1004","1005","1006","1007","2","3","NetUserModalsSet","NetUserModalsSet function [Network Management]","_win32_netusermodalsset","lmaccess/NetUserModalsSet","netmgmt.netusermodalsset"]
old-location: netmgmt\netusermodalsset.htm
tech.root: NetMgmt
ms.assetid: 9884e076-ee6a-4aca-abe6-a79754667759
ms.date: 12/05/2018
ms.keywords: 0, 1, 1001, 1002, 1003, 1004, 1005, 1006, 1007, 2, 3, NetUserModalsSet, NetUserModalsSet function [Network Management], _win32_netusermodalsset, lmaccess/NetUserModalsSet, netmgmt.netusermodalsset
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
 - NetUserModalsSet
 - lmaccess/NetUserModalsSet
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
 - NetUserModalsSet
---

# NetUserModalsSet function


## -description

The
				<b>NetUserModalsSet</b> function sets global information for all users and global groups in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.

## -parameters

### -param servername [in]

Pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

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
Specifies global password parameters. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_0">USER_MODALS_INFO_0</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Specifies logon server and domain controller information. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_1">USER_MODALS_INFO_1</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Specifies the domain name and identifier. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_2">USER_MODALS_INFO_2</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
Specifies lockout information. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_3">USER_MODALS_INFO_3</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1001"></a><dl>
<dt><b>1001</b></dt>
</dl>
</td>
<td width="60%">
Specifies the minimum allowable password length. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_1001">USER_MODALS_INFO_1001</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1002"></a><dl>
<dt><b>1002</b></dt>
</dl>
</td>
<td width="60%">
Specifies the maximum allowable password age. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_1002">USER_MODALS_INFO_1002</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1003"></a><dl>
<dt><b>1003</b></dt>
</dl>
</td>
<td width="60%">
Specifies the minimum allowable password age. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_1003">USER_MODALS_INFO_1003</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1004"></a><dl>
<dt><b>1004</b></dt>
</dl>
</td>
<td width="60%">
Specifies forced logoff information. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_1004">USER_MODALS_INFO_1004</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1005"></a><dl>
<dt><b>1005</b></dt>
</dl>
</td>
<td width="60%">
Specifies the length of the password history. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_1005">USER_MODALS_INFO_1005</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1006"></a><dl>
<dt><b>1006</b></dt>
</dl>
</td>
<td width="60%">
Specifies the role of the logon server. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_1006">USER_MODALS_INFO_1006</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1007"></a><dl>
<dt><b>1007</b></dt>
</dl>
</td>
<td width="60%">
Specifies domain controller information. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_1007">USER_MODALS_INFO_1007</a> structure.

</td>
</tr>
</table>

### -param buf [in]

Pointer to the buffer that specifies the data. The format of this data depends on the value of the <i>level</i> parameter. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a>.

### -param parm_err [out]

Pointer to a value that receives the index of the first member of the information structure that causes ERROR_INVALID_PARAMETER. If this parameter is <b>NULL</b>, the index is not returned on error. For more information, see the following Remarks section.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The specified parameter is invalid. For more information, see the following Remarks section.

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
<dt><b>NERR_UserNotFound</b></dt>
</dl>
</td>
<td width="60%">
The user name could not be found.

</td>
</tr>
</table>

## -remarks

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management user modal functions. For more information, see 
<a href="/windows/desktop/api/iads/nn-iads-iadsdomain">IADsDomain</a>.

If you call this function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the <a href="/windows/desktop/SecAuthZ/securable-objects">securable object</a>. The default ACL permits only Domain Admins and Account Operators to call this function. On a member server or workstation, only Administrators and Power Users can call this function. For more information, see 
<a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="/windows/desktop/SecAuthZ/access-control-model">Access Control Model</a>.

The security descriptor of the Domain object is used to perform the access check for this function. Typically, callers must have write access to the entire object for calls to this function to succeed.

If the 
<b>NetUserModalsSet</b> function returns ERROR_INVALID_PARAMETER, you can use the <i>parm_err</i> parameter to indicate the first member of the information structure that is invalid. (The information structure begins with USER_MODALS_INFO_ and its format is specified by the <i>level</i> parameter.) The following table lists the values that can be returned in the <i>parm_err</i> parameter and the corresponding structure member that is in error. (The prefix usrmod*_ indicates that the member can begin with multiple prefixes, for example, usrmod2_ or usrmod1002_.)

<table>
<tr>
<th>Value</th>
<th>Member</th>
</tr>
<tr>
<td>MODALS_MIN_PASSWD_LEN_PARMNUM</td>
<td>usrmod*_min_passwd_len</td>
</tr>
<tr>
<td>MODALS_MAX_PASSWD_AGE_PARMNUM</td>
<td>usrmod*_max_passwd_age</td>
</tr>
<tr>
<td>MODALS_MIN_PASSWD_AGE_PARMNUM</td>
<td>usrmod*_min_passwd_age</td>
</tr>
<tr>
<td>MODALS_FORCE_LOGOFF_PARMNUM</td>
<td>usrmod*_force_logoff</td>
</tr>
<tr>
<td>MODALS_PASSWD_HIST_LEN_PARMNUM</td>
<td>usrmod*_password_hist_len</td>
</tr>
<tr>
<td>MODALS_ROLE_PARMNUM</td>
<td>usrmod*_role</td>
</tr>
<tr>
<td>MODALS_PRIMARY_PARMNUM</td>
<td>usrmod*_primary</td>
</tr>
<tr>
<td>MODALS_DOMAIN_NAME_PARMNUM</td>
<td>usrmod*_domain_name</td>
</tr>
<tr>
<td>MODALS_DOMAIN_ID_PARMNUM</td>
<td>usrmod*_domain_id</td>
</tr>
<tr>
<td>MODALS_LOCKOUT_DURATION_PARMNUM</td>
<td>usrmod*_lockout_duration</td>
</tr>
<tr>
<td>MODALS_LOCKOUT_OBSERVATION_WINDOW_PARMNUM</td>
<td>usrmod*_lockout_observation_window</td>
</tr>
<tr>
<td>MODALS_LOCKOUT_THRESHOLD_PARMNUM</td>
<td>usrmod*_lockout_threshold</td>
</tr>
</table>
 


#### Examples

The following code sample demonstrates how to set the global information for all users and global groups with a call to the 
<b>NetUserModalsSet</b> function. The sample fills in the members of the 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_0">USER_MODALS_INFO_0</a> structure and calls 
<b>NetUserModalsSet</b>, specifying information level 0.


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
   DWORD dwLevel = 0;
   USER_MODALS_INFO_0 ui;
   NET_API_STATUS nStatus;
   LPTSTR pszServerName = NULL;

   if (argc > 2)
   {
      fwprintf(stderr, L"Usage: %s [\\\\ServerName]\n", argv[0]);
      exit(1);
   }
   // The server is not the default local computer.
   //
   if (argc == 2)
      pszServerName = (LPTSTR) argv[1];
   //
   // Fill in the USER_MODALS_INFO_0 structure.
   //
   ui.usrmod0_min_passwd_len = 0;
   ui.usrmod0_max_passwd_age = (86400 * 30);
   ui.usrmod0_min_passwd_age = 0;
   ui.usrmod0_force_logoff = TIMEQ_FOREVER; // never force logoff
   ui.usrmod0_password_hist_len = 0;
   //
   // Call the NetUserModalsSet function; specify level 0.
   //
   nStatus = NetUserModalsSet((LPCWSTR) pszServerName,
                              dwLevel,
                              (LPBYTE)&ui,
                              NULL);
   //
   // If the call succeeds, inform the user.
   //
   if (nStatus == NERR_Success)
      fwprintf(stderr, L"Modals information set successfully on %s\n", argv[1]);
   //
   // Otherwise, print the system error.
   //
   else
      fprintf(stderr, "A system error has occurred: %d\n", nStatus);

   return 0;
}

```

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusermodalsget">NetUserModalsGet</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_0">USER_MODALS_INFO_0</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_1">USER_MODALS_INFO_1</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_1001">USER_MODALS_INFO_1001</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_1002">USER_MODALS_INFO_1002</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_1003">USER_MODALS_INFO_1003</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_1004">USER_MODALS_INFO_1004</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_1005">USER_MODALS_INFO_1005</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_1006">USER_MODALS_INFO_1006</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_1007">USER_MODALS_INFO_1007</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_2">USER_MODALS_INFO_2</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_3">USER_MODALS_INFO_3</a>



<a href="/windows/desktop/NetMgmt/user-modal-functions">User Modals
		  Functions</a>