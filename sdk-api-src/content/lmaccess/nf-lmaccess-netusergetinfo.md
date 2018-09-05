---
UID: NF:lmaccess.NetUserGetInfo
title: NetUserGetInfo function
author: windows-sdk-content
description: The NetUserGetInfo function retrieves information about a particular user account on a server.
old-location: netmgmt\netusergetinfo.htm
old-project: netmgmt
ms.assetid: 5bd13bed-938a-4273-840e-99fca99f7139
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: 0, 1, 10, 11, 2, 20, 23, 24, 3, 4, NetUserGetInfo, NetUserGetInfo function [Network Management], _win32_netusergetinfo, lmaccess/NetUserGetInfo, netmgmt.netusergetinfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: lmaccess.h
req.include-header: Lm.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - NetUserGetInfo
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# NetUserGetInfo function


## -description


The
				<b>NetUserGetInfo</b> function retrieves information about a particular user account on a server.


## -parameters




### -param servername [in]

A pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.


### -param username [in]

A pointer to a constant string that specifies the name of the user account for which to return information. For more information, see the following Remarks section.


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
Return the user account name. The <i>bufptr</i> parameter points to a 
<a href="https://msdn.microsoft.com/5d24a2dd-d1ee-4c97-8fbc-0b336313b60c">USER_INFO_0</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Return detailed information about the user account. The <i>bufptr</i> parameter points to a 
<a href="https://msdn.microsoft.com/f17a1aef-45f1-461f-975d-75221d08277c">USER_INFO_1</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Return detailed information and additional attributes about the user account. The <i>bufptr</i> parameter points to a 
<a href="https://msdn.microsoft.com/50c78c6a-a08f-473b-929a-9528e618165f">USER_INFO_2</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
Return detailed information and additional attributes about the user account. This level is valid only on servers. The <i>bufptr</i> parameter points to a 
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
Return detailed information and additional attributes about the user account. This level is valid only on servers. The <i>bufptr</i> parameter points to a 
<a href="https://msdn.microsoft.com/66b11a5f-1c2d-4564-8845-9e2fa1f40f3e">USER_INFO_4</a> structure.

<div class="alert"><b>Note</b>  This level is supported on  Windows XP and later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="10"></a><dl>
<dt><b>10</b></dt>
</dl>
</td>
<td width="60%">
Return user and account names and comments. The <i>bufptr</i>  parameter points to a 
<a href="https://msdn.microsoft.com/f85e3e92-02b2-4ee8-8a82-38e4ef5b4072">USER_INFO_10</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="11"></a><dl>
<dt><b>11</b></dt>
</dl>
</td>
<td width="60%">
Return detailed information about the user account. The <i>bufptr</i> parameter points to a 
<a href="https://msdn.microsoft.com/718e7143-a6df-4912-954c-cc63bb490044">USER_INFO_11</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="20"></a><dl>
<dt><b>20</b></dt>
</dl>
</td>
<td width="60%">
Return the user's name and identifier and various account attributes. The <i>bufptr</i> parameter points to a 
<a href="https://msdn.microsoft.com/67f58d6b-488b-4a88-808f-edb9c3464d85">USER_INFO_20</a> structure. Note that on Windows XP and later, it is recommended that you use 
<a href="https://msdn.microsoft.com/1af3ff6d-bc9f-44ad-9981-124ac1961298">USER_INFO_23</a> instead.

</td>
</tr>
<tr>
<td width="40%"><a id="23"></a><dl>
<dt><b>23</b></dt>
</dl>
</td>
<td width="60%">
Return the user's name and identifier and various account attributes. The <i>bufptr</i> parameter points to a 
<a href="https://msdn.microsoft.com/1af3ff6d-bc9f-44ad-9981-124ac1961298">USER_INFO_23</a> structure.

<div class="alert"><b>Note</b>  This level is supported on  Windows XP and later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="24"></a><dl>
<dt><b>24</b></dt>
</dl>
</td>
<td width="60%">
Return user account information for accounts  which are connected to an Internet identity. The <i>bufptr</i> parameter points to a 
<a href="https://msdn.microsoft.com/CE65EDE0-F4AE-4582-9D7F-6667BBA98C75">USER_INFO_24</a> structure.

<div class="alert"><b>Note</b>  The level is supported on Windows 8 and Windows Server 2012.</div>
<div> </div>
</td>
</tr>
</table>
 


### -param bufptr [out]

A pointer to the buffer that receives the data. The format of this data depends on the value of the <i>level</i> parameter. This buffer is allocated by the system and must be freed using the 
<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a> function. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a> and 
<a href="https://msdn.microsoft.com/08599966-68a1-420b-bbc7-6daac833d08f">Network Management Function Buffer Lengths</a>.


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
The network path specified in the <i>servername</i> parameter was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
The value specified for the <i>level</i> parameter is invalid.

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



If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management user functions. For more information, see 
<a href="https://msdn.microsoft.com/6eea74c2-2d6d-4dfd-9a22-3da2d5ce49bf">IADsUser</a> and 
<a href="https://msdn.microsoft.com/e2b90a98-5777-42c2-95dd-4623e738c4da">IADsComputer</a>.

If you call this function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the <a href="https://msdn.microsoft.com/32f2ec06-822f-4d1e-bf51-5ae1d7355e60">securable object</a>. The default ACL permits all authenticated users and members of the "<a href="security.pre_windows_2000_compatible_access_group">Pre-Windows 2000 compatible access</a>" group to view the information. If you call this function on a member server or workstation, all authenticated users can view the information. For  information about anonymous access and restricting anonymous access on these platforms, see 
<a href="https://msdn.microsoft.com/846a5b81-d5bf-4275-a898-38e6ba308b8f">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="https://msdn.microsoft.com/fd3b718a-5eff-4894-9fc6-d157ddb67330">Access Control Model</a>.

The security descriptor of the User object is used to perform the access check for this function.

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.

If the information level specified in the <i>level</i> parameter is set to 24, the <i>servername</i> parameter specified must resolve to the local computer. If the <i>servername</i> resolves to a remote computer or to a domain controller, the <b>NetUserGetInfo</b>  function will fail.


#### Examples

The following code sample demonstrates how to retrieve information about a particular user account with a call to the 
<b>NetUserGetInfo</b> function. The sample calls 
<b>NetUserGetInfo</b>, specifying various information levels . If the call succeeds, the code prints information about the user account. Finally, the sample frees the memory allocated for the information buffer.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#ifndef UNICODE
#define UNICODE
#endif
#pragma comment(lib, "advapi32.lib")
#pragma comment(lib, "netapi32.lib")

#include &lt;windows.h&gt;
#include &lt;stdio.h&gt;
#include &lt;assert.h&gt;
#include &lt;lm.h&gt;
#include &lt;sddl.h&gt;               /* for ConvertSidToStringSid function */

int wmain(int argc, wchar_t * argv[])
{
    DWORD dwLevel = 0;

    LPUSER_INFO_0 pBuf = NULL;
    LPUSER_INFO_1 pBuf1 = NULL;
    LPUSER_INFO_2 pBuf2 = NULL;
    LPUSER_INFO_3 pBuf3 = NULL;
    LPUSER_INFO_4 pBuf4 = NULL;
    LPUSER_INFO_10 pBuf10 = NULL;
    LPUSER_INFO_11 pBuf11 = NULL;
    LPUSER_INFO_20 pBuf20 = NULL;
    LPUSER_INFO_23 pBuf23 = NULL;

    NET_API_STATUS nStatus;

    LPTSTR sStringSid = NULL;

    int i = 0;
    int j = 0;

    if (argc != 3) 
    {
        fwprintf(stderr, L"Usage: %s \\\\ServerName UserName\n", argv[0]);
        exit(1);
    }

    while (i &lt; 24) 
    {

        //
        // Call the NetUserGetInfo function.
        //
        dwLevel = i;
        wprintf
            (L"\nCalling NetUserGetinfo with Servername=%s Username=%s Level=%d\n",
             argv[1], argv[2], dwLevel);
        nStatus = NetUserGetInfo(argv[1], argv[2], dwLevel, (LPBYTE *) &amp; pBuf);
        //
        // If the call succeeds, print the user information.
        //
        if (nStatus == NERR_Success) 
        {
            if (pBuf != NULL) 
            {

                switch (i) 
                {
                case 0:
                    wprintf(L"\tUser account name: %s\n", pBuf-&gt;usri0_name);
                    break;
                case 1:
                    pBuf1 = (LPUSER_INFO_1) pBuf;
                    wprintf(L"\tUser account name: %s\n", pBuf1-&gt;usri1_name);
                    wprintf(L"\tPassword: %s\n", pBuf1-&gt;usri1_password);
                    wprintf(L"\tPassword age (seconds): %d\n",
                            pBuf1-&gt;usri1_password_age);
                    wprintf(L"\tPrivilege level: %d\n", pBuf1-&gt;usri1_priv);
                    wprintf(L"\tHome directory: %s\n", pBuf1-&gt;usri1_home_dir);
                    wprintf(L"\tUser comment: %s\n", pBuf1-&gt;usri1_comment);
                    wprintf(L"\tFlags (in hex): %x\n", pBuf1-&gt;usri1_flags);
                    wprintf(L"\tScript path: %s\n", pBuf1-&gt;usri1_script_path);
                    break;
                case 2:
                    pBuf2 = (LPUSER_INFO_2) pBuf;
                    wprintf(L"\tUser account name: %s\n", pBuf2-&gt;usri2_name);
                    wprintf(L"\tPassword: %s\n", pBuf2-&gt;usri2_password);
                    wprintf(L"\tPassword age (seconds): %d\n",
                            pBuf2-&gt;usri2_password_age);
                    wprintf(L"\tPrivilege level: %d\n", pBuf2-&gt;usri2_priv);
                    wprintf(L"\tHome directory: %s\n", pBuf2-&gt;usri2_home_dir);
                    wprintf(L"\tComment: %s\n", pBuf2-&gt;usri2_comment);
                    wprintf(L"\tFlags (in hex): %x\n", pBuf2-&gt;usri2_flags);
                    wprintf(L"\tScript path: %s\n", pBuf2-&gt;usri2_script_path);
                    wprintf(L"\tAuth flags (in hex): %x\n",
                            pBuf2-&gt;usri2_auth_flags);
                    wprintf(L"\tFull name: %s\n", pBuf2-&gt;usri2_full_name);
                    wprintf(L"\tUser comment: %s\n", pBuf2-&gt;usri2_usr_comment);
                    wprintf(L"\tParameters: %s\n", pBuf2-&gt;usri2_parms);
                    wprintf(L"\tWorkstations: %s\n", pBuf2-&gt;usri2_workstations);
                    wprintf
                        (L"\tLast logon (seconds since January 1, 1970 GMT): %d\n",
                         pBuf2-&gt;usri2_last_logon);
                    wprintf
                        (L"\tLast logoff (seconds since January 1, 1970 GMT): %d\n",
                         pBuf2-&gt;usri2_last_logoff);
                    wprintf
                        (L"\tAccount expires (seconds since January 1, 1970 GMT): %d\n",
                         pBuf2-&gt;usri2_acct_expires);
                    wprintf(L"\tMax storage: %d\n", pBuf2-&gt;usri2_max_storage);
                    wprintf(L"\tUnits per week: %d\n",
                            pBuf2-&gt;usri2_units_per_week);
                    wprintf(L"\tLogon hours:");
                    for (j = 0; j &lt; 21; j++) 
                    {
                        printf(" %x", (BYTE) pBuf2-&gt;usri2_logon_hours[j]);
                    }
                    wprintf(L"\n");
                    wprintf(L"\tBad password count: %d\n",
                            pBuf2-&gt;usri2_bad_pw_count);
                    wprintf(L"\tNumber of logons: %d\n",
                            pBuf2-&gt;usri2_num_logons);
                    wprintf(L"\tLogon server: %s\n", pBuf2-&gt;usri2_logon_server);
                    wprintf(L"\tCountry code: %d\n", pBuf2-&gt;usri2_country_code);
                    wprintf(L"\tCode page: %d\n", pBuf2-&gt;usri2_code_page);
                    break;
                case 4:
                    pBuf4 = (LPUSER_INFO_4) pBuf;
                    wprintf(L"\tUser account name: %s\n", pBuf4-&gt;usri4_name);
                    wprintf(L"\tPassword: %s\n", pBuf4-&gt;usri4_password);
                    wprintf(L"\tPassword age (seconds): %d\n",
                            pBuf4-&gt;usri4_password_age);
                    wprintf(L"\tPrivilege level: %d\n", pBuf4-&gt;usri4_priv);
                    wprintf(L"\tHome directory: %s\n", pBuf4-&gt;usri4_home_dir);
                    wprintf(L"\tComment: %s\n", pBuf4-&gt;usri4_comment);
                    wprintf(L"\tFlags (in hex): %x\n", pBuf4-&gt;usri4_flags);
                    wprintf(L"\tScript path: %s\n", pBuf4-&gt;usri4_script_path);
                    wprintf(L"\tAuth flags (in hex): %x\n",
                            pBuf4-&gt;usri4_auth_flags);
                    wprintf(L"\tFull name: %s\n", pBuf4-&gt;usri4_full_name);
                    wprintf(L"\tUser comment: %s\n", pBuf4-&gt;usri4_usr_comment);
                    wprintf(L"\tParameters: %s\n", pBuf4-&gt;usri4_parms);
                    wprintf(L"\tWorkstations: %s\n", pBuf4-&gt;usri4_workstations);
                    wprintf
                        (L"\tLast logon (seconds since January 1, 1970 GMT): %d\n",
                         pBuf4-&gt;usri4_last_logon);
                    wprintf
                        (L"\tLast logoff (seconds since January 1, 1970 GMT): %d\n",
                         pBuf4-&gt;usri4_last_logoff);
                    wprintf
                        (L"\tAccount expires (seconds since January 1, 1970 GMT): %d\n",
                         pBuf4-&gt;usri4_acct_expires);
                    wprintf(L"\tMax storage: %d\n", pBuf4-&gt;usri4_max_storage);
                    wprintf(L"\tUnits per week: %d\n",
                            pBuf4-&gt;usri4_units_per_week);
                    wprintf(L"\tLogon hours:");
                    for (j = 0; j &lt; 21; j++) 
                    {
                        printf(" %x", (BYTE) pBuf4-&gt;usri4_logon_hours[j]);
                    }
                    wprintf(L"\n");
                    wprintf(L"\tBad password count: %d\n",
                            pBuf4-&gt;usri4_bad_pw_count);
                    wprintf(L"\tNumber of logons: %d\n",
                            pBuf4-&gt;usri4_num_logons);
                    wprintf(L"\tLogon server: %s\n", pBuf4-&gt;usri4_logon_server);
                    wprintf(L"\tCountry code: %d\n", pBuf4-&gt;usri4_country_code);
                    wprintf(L"\tCode page: %d\n", pBuf4-&gt;usri4_code_page);
                    if (ConvertSidToStringSid
                        (pBuf4-&gt;usri4_user_sid, &amp;sStringSid)) 
                    {
                        wprintf(L"\tUser SID: %s\n", sStringSid);
                        LocalFree(sStringSid);
                    } 
                    else
                        wprintf(L"ConvertSidToSTringSid failed with error %d\n",
                                GetLastError());
                    wprintf(L"\tPrimary group ID: %d\n",
                            pBuf4-&gt;usri4_primary_group_id);
                    wprintf(L"\tProfile: %s\n", pBuf4-&gt;usri4_profile);
                    wprintf(L"\tHome directory drive letter: %s\n",
                            pBuf4-&gt;usri4_home_dir_drive);
                    wprintf(L"\tPassword expired information: %d\n",
                            pBuf4-&gt;usri4_password_expired);
                    break;
                case 10:
                    pBuf10 = (LPUSER_INFO_10) pBuf;
                    wprintf(L"\tUser account name: %s\n", pBuf10-&gt;usri10_name);
                    wprintf(L"\tComment: %s\n", pBuf10-&gt;usri10_comment);
                    wprintf(L"\tUser comment: %s\n",
                            pBuf10-&gt;usri10_usr_comment);
                    wprintf(L"\tFull name: %s\n", pBuf10-&gt;usri10_full_name);
                    break;
                case 11:
                    pBuf11 = (LPUSER_INFO_11) pBuf;
                    wprintf(L"\tUser account name: %s\n", pBuf11-&gt;usri11_name);
                    wprintf(L"\tComment: %s\n", pBuf11-&gt;usri11_comment);
                    wprintf(L"\tUser comment: %s\n",
                            pBuf11-&gt;usri11_usr_comment);
                    wprintf(L"\tFull name: %s\n", pBuf11-&gt;usri11_full_name);
                    wprintf(L"\tPrivilege level: %d\n", pBuf11-&gt;usri11_priv);
                    wprintf(L"\tAuth flags (in hex): %x\n",
                            pBuf11-&gt;usri11_auth_flags);
                    wprintf(L"\tPassword age (seconds): %d\n",
                            pBuf11-&gt;usri11_password_age);
                    wprintf(L"\tHome directory: %s\n", pBuf11-&gt;usri11_home_dir);
                    wprintf(L"\tParameters: %s\n", pBuf11-&gt;usri11_parms);
                    wprintf
                        (L"\tLast logon (seconds since January 1, 1970 GMT): %d\n",
                         pBuf11-&gt;usri11_last_logon);
                    wprintf
                        (L"\tLast logoff (seconds since January 1, 1970 GMT): %d\n",
                         pBuf11-&gt;usri11_last_logoff);
                    wprintf(L"\tBad password count: %d\n",
                            pBuf11-&gt;usri11_bad_pw_count);
                    wprintf(L"\tNumber of logons: %d\n",
                            pBuf11-&gt;usri11_num_logons);
                    wprintf(L"\tLogon server: %s\n",
                            pBuf11-&gt;usri11_logon_server);
                    wprintf(L"\tCountry code: %d\n",
                            pBuf11-&gt;usri11_country_code);
                    wprintf(L"\tWorkstations: %s\n",
                            pBuf11-&gt;usri11_workstations);
                    wprintf(L"\tMax storage: %d\n", pBuf11-&gt;usri11_max_storage);
                    wprintf(L"\tUnits per week: %d\n",
                            pBuf11-&gt;usri11_units_per_week);
                    wprintf(L"\tLogon hours:");
                    for (j = 0; j &lt; 21; j++) 
                    {
                        printf(" %x", (BYTE) pBuf11-&gt;usri11_logon_hours[j]);
                    }
                    wprintf(L"\n");
                    wprintf(L"\tCode page: %d\n", pBuf11-&gt;usri11_code_page);
                    break;
                case 20:
                    pBuf20 = (LPUSER_INFO_20) pBuf;
                    wprintf(L"\tUser account name: %s\n", pBuf20-&gt;usri20_name);
                    wprintf(L"\tFull name: %s\n", pBuf20-&gt;usri20_full_name);
                    wprintf(L"\tComment: %s\n", pBuf20-&gt;usri20_comment);
                    wprintf(L"\tFlags (in hex): %x\n", pBuf20-&gt;usri20_flags);
                    wprintf(L"\tUser ID: %u\n", pBuf20-&gt;usri20_user_id);
                    break;
                case 23:
                    pBuf23 = (LPUSER_INFO_23) pBuf;
                    wprintf(L"\tUser account name: %s\n", pBuf23-&gt;usri23_name);
                    wprintf(L"\tFull name: %s\n", pBuf23-&gt;usri23_full_name);
                    wprintf(L"\tComment: %s\n", pBuf23-&gt;usri23_comment);
                    wprintf(L"\tFlags (in hex): %x\n", pBuf23-&gt;usri23_flags);
                    if (ConvertSidToStringSid
                        (pBuf23-&gt;usri23_user_sid, &amp;sStringSid)) 
                    {
                        wprintf(L"\tUser SID: %s\n", sStringSid);
                        LocalFree(sStringSid);
                    } 
                    else
                        wprintf(L"ConvertSidToSTringSid failed with error %d\n",
                                GetLastError());
                    break;
                default:
                    break;
                }
            }
        }
        // Otherwise, print the system error.
        //
        else
            fprintf(stderr, "NetUserGetinfo failed with error: %d\n", nStatus);
        //
        // Free the allocated memory.
        //
        if (pBuf != NULL)
            NetApiBufferFree(pBuf);

        switch (i) 
        {
        case 0:
        case 1:
        case 10:
            i++;
            break;
        case 2:
            i = 4;
            break;
        case 4:
            i = 10;
            break;
        case 11:
            i = 20;
            break;
        case 20:
            i = 23;
            break;
        default:
            i = 24;
            break;
        }
    }
    return 0;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b26ef3c0-934a-4840-8c06-4eaff5c9ff86">NetUserEnum</a>



<a href="https://msdn.microsoft.com/ecf1a94c-5dda-4f49-81bd-93e551e089f1">NetUserGetGroups</a>



<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/5d24a2dd-d1ee-4c97-8fbc-0b336313b60c">USER_INFO_0</a>



<a href="https://msdn.microsoft.com/f17a1aef-45f1-461f-975d-75221d08277c">USER_INFO_1</a>



<a href="https://msdn.microsoft.com/f85e3e92-02b2-4ee8-8a82-38e4ef5b4072">USER_INFO_10</a>



<a href="https://msdn.microsoft.com/718e7143-a6df-4912-954c-cc63bb490044">USER_INFO_11</a>



<a href="https://msdn.microsoft.com/50c78c6a-a08f-473b-929a-9528e618165f">USER_INFO_2</a>



<a href="https://msdn.microsoft.com/1af3ff6d-bc9f-44ad-9981-124ac1961298">USER_INFO_23</a>



<a href="https://msdn.microsoft.com/CE65EDE0-F4AE-4582-9D7F-6667BBA98C75">USER_INFO_24</a>



<a href="https://msdn.microsoft.com/66b11a5f-1c2d-4564-8845-9e2fa1f40f3e">USER_INFO_4</a>



<a href="https://msdn.microsoft.com/cf0e5102-3924-46c0-8124-0aa04e95f48d">User Functions</a>
 

 

