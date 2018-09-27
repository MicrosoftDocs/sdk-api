---
UID: NF:lmaccess.NetUserEnum
title: NetUserEnum function
author: windows-sdk-content
description: The NetUserEnum function retrieves information about all user accounts on a server.
old-location: netmgmt\netuserenum.htm
tech.root: netmgmt
ms.assetid: b26ef3c0-934a-4840-8c06-4eaff5c9ff86
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: 0, 1, 10, 11, 2, 20, 3, FILTER_INTERDOMAIN_TRUST_ACCOUNT, FILTER_NORMAL_ACCOUNT, FILTER_SERVER_TRUST_ACCOUNT, FILTER_TEMP_DUPLICATE_ACCOUNT, FILTER_WORKSTATION_TRUST_ACCOUNT, NetUserEnum, NetUserEnum function [Network Management], _win32_netuserenum, lmaccess/NetUserEnum, netmgmt.netuserenum
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
 - NetUserEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NetUserEnum function


## -description


The
				<b>NetUserEnum</b> function retrieves information about all user accounts on a server.


## -parameters




### -param servername [in]

A pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.


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
Return user account names. The <i>bufptr</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/5d24a2dd-d1ee-4c97-8fbc-0b336313b60c">USER_INFO_0</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Return detailed information about user accounts. The <i>bufptr</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/f17a1aef-45f1-461f-975d-75221d08277c">USER_INFO_1</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Return detailed information about user accounts, including authorization levels and logon information. The <i>bufptr</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/50c78c6a-a08f-473b-929a-9528e618165f">USER_INFO_2</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
Return detailed information about user accounts, including authorization levels, logon information, RIDs for the user and the primary group, and profile information. The <i>bufptr</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/39ed05f5-165d-4cb8-98af-e4120a1634f6">USER_INFO_3</a> structures. 

</td>
</tr>
<tr>
<td width="40%"><a id="10"></a><dl>
<dt><b>10</b></dt>
</dl>
</td>
<td width="60%">
Return user and account names and comments. The <i>bufptr</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/f85e3e92-02b2-4ee8-8a82-38e4ef5b4072">USER_INFO_10</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="11"></a><dl>
<dt><b>11</b></dt>
</dl>
</td>
<td width="60%">
Return detailed information about user accounts. The <i>bufptr</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/718e7143-a6df-4912-954c-cc63bb490044">USER_INFO_11</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="20"></a><dl>
<dt><b>20</b></dt>
</dl>
</td>
<td width="60%">
Return the user's name and identifier and various account attributes. The <i>bufptr</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/67f58d6b-488b-4a88-808f-edb9c3464d85">USER_INFO_20</a> structures. Note that on Windows XP and later, it is recommended that you use 
<a href="https://msdn.microsoft.com/1af3ff6d-bc9f-44ad-9981-124ac1961298">USER_INFO_23</a> instead.

</td>
</tr>
</table>
 


### -param filter [in]

A value that specifies the user account types to be included in the enumeration. A value of zero indicates that all normal user, trust data, and machine account data should be included. 

This parameter can also be a combination of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILTER_TEMP_DUPLICATE_ACCOUNT"></a><a id="filter_temp_duplicate_account"></a><dl>
<dt><b>FILTER_TEMP_DUPLICATE_ACCOUNT</b></dt>
</dl>
</td>
<td width="60%">
Enumerates account data for users whose primary account is in another domain. This account type provides user access to this domain, but not to any domain that trusts this domain. The User Manager refers to this account type as a local user account.

</td>
</tr>
<tr>
<td width="40%"><a id="FILTER_NORMAL_ACCOUNT"></a><a id="filter_normal_account"></a><dl>
<dt><b>FILTER_NORMAL_ACCOUNT</b></dt>
</dl>
</td>
<td width="60%">
Enumerates normal user account data. This account type is associated with a typical user.

</td>
</tr>
<tr>
<td width="40%"><a id="FILTER_INTERDOMAIN_TRUST_ACCOUNT"></a><a id="filter_interdomain_trust_account"></a><dl>
<dt><b>FILTER_INTERDOMAIN_TRUST_ACCOUNT</b></dt>
</dl>
</td>
<td width="60%">
Enumerates interdomain trust account data. This account type is associated with a trust account for a domain that trusts other domains.

</td>
</tr>
<tr>
<td width="40%"><a id="FILTER_WORKSTATION_TRUST_ACCOUNT"></a><a id="filter_workstation_trust_account"></a><dl>
<dt><b>FILTER_WORKSTATION_TRUST_ACCOUNT</b></dt>
</dl>
</td>
<td width="60%">
Enumerates workstation or member server trust account data. This account type is associated with a machine account for a computer that is a member of the domain.

</td>
</tr>
<tr>
<td width="40%"><a id="FILTER_SERVER_TRUST_ACCOUNT"></a><a id="filter_server_trust_account"></a><dl>
<dt><b>FILTER_SERVER_TRUST_ACCOUNT</b></dt>
</dl>
</td>
<td width="60%">
Enumerates member server machine account data. This account type is associated with a computer account for a backup domain controller that is a member of the domain.

</td>
</tr>
</table>
 


### -param bufptr [out]

A pointer to the buffer that receives the data. The format of this data depends on the value of the <i>level</i> parameter. 

The buffer for this data is allocated by the system and the application must call the <a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a> function to free the allocated memory when the data returned is no longer needed. Note that you must free the buffer even if the <b>NetUserEnum</b> function fails with ERROR_MORE_DATA.


### -param prefmaxlen [in]

The preferred maximum length, in bytes, of the returned data. If you specify MAX_PREFERRED_LENGTH, the <b>NetUserEnum</b> function allocates the amount of memory required for the data. If you specify another value in this parameter, it can restrict the number of bytes that the function returns. If the buffer size is insufficient to hold all entries, the function returns ERROR_MORE_DATA. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a> and 
<a href="https://msdn.microsoft.com/08599966-68a1-420b-bbc7-6daac833d08f">Network Management Function Buffer Lengths</a>.


### -param entriesread [out]

A pointer to a value that receives the count of elements actually enumerated.


### -param totalentries [out]

A pointer to a value that receives the total number of entries that could have been enumerated from the current resume position. Note that applications should consider this value only as a hint. If your application is communicating with a Windows 2000 or later domain controller, you should consider using the 
<a href="https://msdn.microsoft.com/3c13ea2f-fe40-4fd4-8540-422f277e07c1">ADSI LDAP Provider</a> to retrieve this type of data more efficiently. The ADSI LDAP Provider implements a set of ADSI objects that support various ADSI interfaces. For more information, see 
<a href="https://msdn.microsoft.com/419d7953-a879-4d6c-be74-173d76c3f932">ADSI Service Providers</a>. 




<b>LAN Manager:  </b>If the call is to a computer that is running LAN Manager 2.<i>x</i>, the <i>totalentries</i> parameter will always reflect the total number of entries in the database no matter where it is in the resume sequence.


### -param resume_handle [in, out]

A pointer to a value that contains a resume handle which is used to continue an existing user search. The handle should be zero on the first call and left unchanged for subsequent calls. If this parameter is <b>NULL</b>, then no resume handle is stored.


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
The system call level is not correct. This error is returned if the <i>level</i> parameter is set to a value not supported. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_BufTooSmall</b></dt>
</dl>
</td>
<td width="60%">
The buffer is too small to contain an entry. No information has been written to the buffer. 

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
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
More entries are available. Specify a large enough buffer to receive all entries.

</td>
</tr>
</table>
 




## -remarks



The
				<b>NetUserEnum</b> function retrieves information about all user accounts on a specified remote server or the local computer.

The 
<a href="https://msdn.microsoft.com/049f1ea3-4d23-4b35-8b08-7256859aed45">NetQueryDisplayInformation</a> function can be used to quickly enumerate user, computer, or global group account information for display in user interfaces .

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management user functions. For more information, see 
<a href="https://msdn.microsoft.com/6eea74c2-2d6d-4dfd-9a22-3da2d5ce49bf">IADsUser</a> and 
<a href="https://msdn.microsoft.com/e2b90a98-5777-42c2-95dd-4623e738c4da">IADsComputer</a>.

If you call the <b>NetUserEnum</b> function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the <a href="https://msdn.microsoft.com/32f2ec06-822f-4d1e-bf51-5ae1d7355e60">securable object</a>. The default ACL permits all authenticated users and members of the "<a href="https://msdn.microsoft.com/library/Aa375347(v=VS.85).aspx">Pre-Windows 2000 compatible access</a>" group to view the information. If you call this function on a member server or workstation, all authenticated users can view the information. For  information about anonymous access and restricting anonymous access on these platforms, see 
<a href="https://msdn.microsoft.com/846a5b81-d5bf-4275-a898-38e6ba308b8f">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="https://msdn.microsoft.com/fd3b718a-5eff-4894-9fc6-d157ddb67330">Access Control Model</a>.

The <b>NetUserEnum</b> function only returns information to which the caller has Read access. The caller must have List Contents access to the Domain object, and  Enumerate Entire SAM Domain access on the SAM Server object  located in the System container. 

The <a href="https://msdn.microsoft.com/5c371d5a-26cf-4a99-a8e1-006b6b3cc91f">LsaEnumerateTrustedDomains</a> or <a href="https://msdn.microsoft.com/4a203bff-c3e1-4d95-b556-617dc8c2e8c2">LsaEnumerateTrustedDomainsEx</a> function can be used to retrieve the names and SIDs of domains trusted by a Local Security Authority (LSA) policy object.

The 
<b>NetUserEnum</b> function does not return all system users. It returns only those users who have been added with a call to the 
<a href="https://msdn.microsoft.com/b5ca5f76-d40b-4abf-925a-0de54fc476e4">NetUserAdd</a> function. There is no guarantee that the list of users will be returned in sorted order.

If you call 
the <b>NetUserEnum</b> function and specify information level 1, 2, or 3,  for the <i>level</i> parameter, the password member of each structure retrieved is set to <b>NULL</b> to maintain password security.  

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.

The <b>NetUserEnum</b> function does not support a <i>level</i> parameter of 4 and the <a href="https://msdn.microsoft.com/66b11a5f-1c2d-4564-8845-9e2fa1f40f3e">USER_INFO_4</a> structure. The <a href="https://msdn.microsoft.com/5bd13bed-938a-4273-840e-99fca99f7139">NetUserGetInfo</a> 
		function supports a <i>level</i> parameter of 4 and the <b>USER_INFO_4</b> structure.


#### Examples

The following code sample demonstrates how to retrieve information about the user accounts on a server with a call to the 
<b>NetUserEnum</b> function. The sample calls 
<b>NetUserEnum</b>, specifying information level 0 (<a href="https://msdn.microsoft.com/5d24a2dd-d1ee-4c97-8fbc-0b336313b60c">USER_INFO_0</a>) to enumerate only global user accounts. If the call succeeds, the code loops through the entries and prints the name of each user account. Finally, the code sample frees the memory allocated for the information buffer and prints a total of the users enumerated.


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
   LPUSER_INFO_0 pBuf = NULL;
   LPUSER_INFO_0 pTmpBuf;
   DWORD dwLevel = 0;
   DWORD dwPrefMaxLen = MAX_PREFERRED_LENGTH;
   DWORD dwEntriesRead = 0;
   DWORD dwTotalEntries = 0;
   DWORD dwResumeHandle = 0;
   DWORD i;
   DWORD dwTotalCount = 0;
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
      pszServerName =  (LPTSTR) argv[1];
   wprintf(L"\nUser account on %s: \n", pszServerName);
   //
   // Call the NetUserEnum function, specifying level 0; 
   //   enumerate global user account types only.
   //
   do // begin do
   {
      nStatus = NetUserEnum((LPCWSTR) pszServerName,
                            dwLevel,
                            FILTER_NORMAL_ACCOUNT, // global users
                            (LPBYTE*)&pBuf,
                            dwPrefMaxLen,
                            &dwEntriesRead,
                            &dwTotalEntries,
                            &dwResumeHandle);
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
            for (i = 0; (i < dwEntriesRead); i++)
            {
               assert(pTmpBuf != NULL);

               if (pTmpBuf == NULL)
               {
                  fprintf(stderr, "An access violation has occurred\n");
                  break;
               }
               //
               //  Print the name of the user account.
               //
               wprintf(L"\t-- %s\n", pTmpBuf->usri0_name);

               pTmpBuf++;
               dwTotalCount++;
            }
         }
      }
      //
      // Otherwise, print the system error.
      //
      else
         fprintf(stderr, "A system error has occurred: %d\n", nStatus);
      //
      // Free the allocated buffer.
      //
      if (pBuf != NULL)
      {
         NetApiBufferFree(pBuf);
         pBuf = NULL;
      }
   }
   // Continue to call NetUserEnum while 
   //  there are more entries. 
   // 
   while (nStatus == ERROR_MORE_DATA); // end do
   //
   // Check again for allocated memory.
   //
   if (pBuf != NULL)
      NetApiBufferFree(pBuf);
   //
   // Print the final count of users enumerated.
   //
   fprintf(stderr, "\nTotal of %d entries enumerated\n", dwTotalCount);

   return 0;
}

```





## -see-also




<a href="https://msdn.microsoft.com/5c371d5a-26cf-4a99-a8e1-006b6b3cc91f">LsaEnumerateTrustedDomains</a>



<a href="https://msdn.microsoft.com/4a203bff-c3e1-4d95-b556-617dc8c2e8c2">LsaEnumerateTrustedDomainsEx</a>



<a href="https://msdn.microsoft.com/049f1ea3-4d23-4b35-8b08-7256859aed45">NetQueryDisplayInformation</a>



<a href="https://msdn.microsoft.com/b5ca5f76-d40b-4abf-925a-0de54fc476e4">NetUserAdd</a>



<a href="https://msdn.microsoft.com/ecf1a94c-5dda-4f49-81bd-93e551e089f1">NetUserGetGroups</a>



<a href="https://msdn.microsoft.com/5bd13bed-938a-4273-840e-99fca99f7139">NetUserGetInfo</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/5d24a2dd-d1ee-4c97-8fbc-0b336313b60c">USER_INFO_0</a>



<a href="https://msdn.microsoft.com/f17a1aef-45f1-461f-975d-75221d08277c">USER_INFO_1</a>



<a href="https://msdn.microsoft.com/f85e3e92-02b2-4ee8-8a82-38e4ef5b4072">USER_INFO_10</a>



<a href="https://msdn.microsoft.com/718e7143-a6df-4912-954c-cc63bb490044">USER_INFO_11</a>



<a href="https://msdn.microsoft.com/50c78c6a-a08f-473b-929a-9528e618165f">USER_INFO_2</a>



<a href="https://msdn.microsoft.com/67f58d6b-488b-4a88-808f-edb9c3464d85">USER_INFO_20</a>



<a href="https://msdn.microsoft.com/1af3ff6d-bc9f-44ad-9981-124ac1961298">USER_INFO_23</a>



<a href="https://msdn.microsoft.com/39ed05f5-165d-4cb8-98af-e4120a1634f6">USER_INFO_3</a>



<a href="https://msdn.microsoft.com/cf0e5102-3924-46c0-8124-0aa04e95f48d">User Functions</a>
 

 

