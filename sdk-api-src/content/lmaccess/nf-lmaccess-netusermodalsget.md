---
UID: NF:lmaccess.NetUserModalsGet
title: NetUserModalsGet function (lmaccess.h)
description: The NetUserModalsGet function retrieves global information for all users and global groups in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.
helpviewer_keywords: ["0","1","2","3","NetUserModalsGet","NetUserModalsGet function [Network Management]","_win32_netusermodalsget","lmaccess/NetUserModalsGet","netmgmt.netusermodalsget"]
old-location: netmgmt\netusermodalsget.htm
tech.root: NetMgmt
ms.assetid: 5bb18144-82a6-4e9b-8321-c06a667bdd03
ms.date: 12/05/2018
ms.keywords: 0, 1, 2, 3, NetUserModalsGet, NetUserModalsGet function [Network Management], _win32_netusermodalsget, lmaccess/NetUserModalsGet, netmgmt.netusermodalsget
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
 - NetUserModalsGet
 - lmaccess/NetUserModalsGet
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
 - NetUserModalsGet
---

# NetUserModalsGet function


## -description

The
				<b>NetUserModalsGet</b> function retrieves global information for all users and global groups in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.

## -parameters

### -param servername [in, optional]

A pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used. For more information, see the following Remarks section.

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
Return global password parameters. The <i>bufptr</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_0">USER_MODALS_INFO_0</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Return logon server and domain controller information. The <i>bufptr</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_1">USER_MODALS_INFO_1</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Return domain name and identifier. The <i>bufptr</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_2">USER_MODALS_INFO_2</a> structure. For more information, see the following Remarks section.

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
Return lockout information. The <i>bufptr</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_3">USER_MODALS_INFO_3</a> structure.

</td>
</tr>
</table>
 

A null session logon can call 
<b>NetUserModalsGet</b> anonymously at information levels 0 and 3.

### -param bufptr [out]

A pointer to the buffer that receives the data. The format of this data depends on the value of the <i>level</i> parameter. 

The buffer for this data is allocated by the system and the application must call the <a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function to free the allocated memory when the data returned is no longer needed. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a> and 
<a href="/windows/desktop/NetMgmt/network-management-function-buffer-lengths">Network Management Function Buffer Lengths</a>.

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
The system call level is not correct. This error is returned if the <i>level </i> parameter is not one of the supported values.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_NAME</b></dt>
</dl>
</td>
<td width="60%">
The file name, directory name, or volume label syntax is incorrect. This error is returned if the <i>servername</i> parameter syntax is incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WRONG_TARGET_NAME</b></dt>
</dl>
</td>
<td width="60%">
The target account name is incorrect. This error is returned for a logon failure to a remote <i>servername</i> parameter running on Windows Vista.

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
</table>

## -remarks

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management user modal functions. For more information, see 
<a href="/windows/desktop/api/iads/nn-iads-iadsdomain">IADsDomain</a>.

If you call this function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the <a href="/windows/desktop/SecAuthZ/securable-objects">securable object</a>. The default ACL permits all authenticated users and members of the "<a href="/windows/desktop/SecAuthZ/allowing-anonymous-access">Pre-Windows 2000 compatible access</a>" group to view the information. If you call this function on a member server or workstation, all authenticated users can view the information. For  information about anonymous access and restricting anonymous access on these platforms, see 
<a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="/windows/desktop/SecAuthZ/access-control-model">Access Control Model</a>.

The security descriptor of the Domain object is used to perform the access check for this function.

To retrieve the 
<a href="/windows/desktop/SecAuthZ/security-identifiers">security identifier</a> (SID) of the domain to which the computer belongs, call the 
<b>NetUserModalsGet</b> function specifying a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_2">USER_MODALS_INFO_2</a> structure and <b>NULL</b> in the <i>servername</i> parameter. If the computer isn't a member of a domain, the function returns a <b>NULL</b> pointer.


#### Examples

The following code sample demonstrates how to retrieve global information for all users and global groups with a call to the 
<b>NetUserModalsGet</b> function. The sample calls 
<b>NetUserModalsGet</b>, specifying information level 0 (<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_0">USER_MODALS_INFO_0</a>). If the call succeeds, the sample prints global password information. Finally, the code sample frees the memory allocated for the information buffer.


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
   USER_MODALS_INFO_0 *pBuf = NULL;
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
   // Call the NetUserModalsGet function; specify level 0.
   //
   nStatus = NetUserModalsGet((LPCWSTR) pszServerName,
                              dwLevel,
                              (LPBYTE *)&pBuf);
   //
   // If the call succeeds, print the global information.
   //
   if (nStatus == NERR_Success)
   {
      if (pBuf != NULL)
      {
         printf("\tMinimum password length:  %d\n", pBuf->usrmod0_min_passwd_len);
         printf("\tMaximum password age (d): %d\n", pBuf->usrmod0_max_passwd_age/86400);
         printf("\tMinimum password age (d): %d\n", pBuf->usrmod0_min_passwd_age/86400);
         printf("\tForced log off time (s):  %d\n", pBuf->usrmod0_force_logoff);
         printf("\tPassword history length:  %d\n", pBuf->usrmod0_password_hist_len);
      }
   }
   // Otherwise, print the system error.
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

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusermodalsset">NetUserModalsSet</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_0">USER_MODALS_INFO_0</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_1">USER_MODALS_INFO_1</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_2">USER_MODALS_INFO_2</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_modals_info_3">USER_MODALS_INFO_3</a>



<a href="/windows/desktop/NetMgmt/user-modal-functions">User Modals
		  Functions</a>