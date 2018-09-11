---
UID: NF:securitybaseapi.CreateRestrictedToken
title: CreateRestrictedToken function
author: windows-sdk-content
description: Creates a new access token that is a restricted version of an existing access token. The restricted token can have disabled security identifiers (SIDs), deleted privileges, and a list of restricting SIDs.
old-location: security\createrestrictedtoken.htm
tech.root: SecAuthZ
ms.assetid: e087f360-5d1d-4846-b3d6-214a426e5222
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CreateRestrictedToken, CreateRestrictedToken function [Security], DISABLE_MAX_PRIVILEGE, LUA_TOKEN, SANDBOX_INERT, WRITE_RESTRICTED, _win32_createrestrictedtoken, security.createrestrictedtoken, securitybaseapi/CreateRestrictedToken
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: securitybaseapi.h
req.include-header: Windows.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - CreateRestrictedToken
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateRestrictedToken function


## -description


The <b>CreateRestrictedToken</b> function creates a new <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access token</a> that is a restricted version of an existing access token. The restricted token can have disabled <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> (SIDs), deleted privileges, and a list of restricting SIDs. For more information, see 
<a href="https://msdn.microsoft.com/06580ab9-ff58-4aa9-bf88-9536a2e1981d">Restricted Tokens</a>.


## -parameters




### -param ExistingTokenHandle [in]

A handle to a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">primary</a> or <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">impersonation token</a>. The token can also be a restricted token. The handle must have TOKEN_DUPLICATE access to the token.


### -param Flags [in]

Specifies additional privilege options. This parameter can be zero or a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DISABLE_MAX_PRIVILEGE"></a><a id="disable_max_privilege"></a><dl>
<dt><b>DISABLE_MAX_PRIVILEGE</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Disables all privileges in the new token except the <b>SeChangeNotifyPrivilege</b> privilege. If this value is specified, the <i>DeletePrivilegeCount</i> and <i>PrivilegesToDelete</i> parameters are ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="SANDBOX_INERT"></a><a id="sandbox_inert"></a><dl>
<dt><b>SANDBOX_INERT</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
If this value is used, the system does not check <a href=" http://go.microsoft.com/fwlink/p/?linkid=161970">AppLocker</a> rules  or apply <a href="http://go.microsoft.com/fwlink/p/?linkid=161971">Software Restriction Policies</a>. For <a href=" http://go.microsoft.com/fwlink/p/?linkid=161970">AppLocker</a>, this flag disables checks for all four rule collections: Executable, Windows Installer, Script, and DLL.

When creating a setup program that must run extracted DLLs during installation, use the flag <b>SAFER_TOKEN_MAKE_INERT</b> in the <a href="https://msdn.microsoft.com/39406331-3101-48f2-8b92-e049849b2b38">SaferComputeTokenFromLevel</a> function.

A token can be queried for existence of this flag by using <a href="https://msdn.microsoft.com/e94de19c-de12-40fb-a72c-060f7ad12f75">GetTokenInformation</a>.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>On systems with KB2532445 installed, the caller must be running as LocalSystem or TrustedInstaller or the system ignores this flag. For more information, see  "You can circumvent AppLocker rules by using an Office macro on a computer that is running Windows 7 or Windows Server 2008 R2" in the Help and Support Knowledge Base at <a href="http://support.microsoft.com/kb/2532445">http://support.microsoft.com/kb/2532445</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>AppLocker is not supported. AppLocker was introduced in Windows 7 and Windows Server 2008 R2.

</td>
</tr>
<tr>
<td width="40%"><a id="LUA_TOKEN"></a><a id="lua_token"></a><dl>
<dt><b>LUA_TOKEN</b></dt>
<dt>0x4</dt>
</dl>
</td>
<td width="60%">
The new token is a LUA token.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="WRITE_RESTRICTED"></a><a id="write_restricted"></a><dl>
<dt><b>WRITE_RESTRICTED</b></dt>
<dt>0x8</dt>
</dl>
</td>
<td width="60%">
The new token contains restricting SIDs that are considered only when evaluating write access.

<b>Windows XP with SP2 and later:  </b>The value of this constant is 0x4. For an application to be compatible with Windows XP with SP2 and later operating systems, the application should query the operating system by calling the <a href="https://msdn.microsoft.com/8e3ab4d6-bacd-4bc5-b8f6-dd49289354de">GetVersionEx</a> function to determine which value should be used.

<b>Windows Server 2003 and Windows XP with SP1 and earlier:  </b>This value is not supported.

</td>
</tr>
</table>
 


### -param DisableSidCount [in]

Specifies the number of entries in the <i>SidsToDisable</i> array.


### -param SidsToDisable [in, optional]

A pointer to an array of 
<a href="https://msdn.microsoft.com/d15d5a3f-6b38-4b92-b59c-ff0d27d111d9">SID_AND_ATTRIBUTES</a> structures that specify the deny-only SIDs in the restricted token. The system uses a deny-only SID to deny access to a securable object. The absence of a deny-only SID does not allow access. 




Disabling a SID turns on SE_GROUP_USE_FOR_DENY_ONLY and turns off SE_GROUP_ENABLED and SE_GROUP_ENABLED_BY_DEFAULT. All other attributes are ignored.

Deny-only attributes apply to any combination of an existing token's SIDs, including the user SID and group SIDs that have the SE_GROUP_MANDATORY attribute. To get the SIDs associated with the existing token, use the 
<a href="https://msdn.microsoft.com/e94de19c-de12-40fb-a72c-060f7ad12f75">GetTokenInformation</a> function with the TokenUser and TokenGroups flags. The function ignores any SIDs in the array that are not also found in the existing token.

The function ignores the <b>Attributes</b> member of the <a href="https://msdn.microsoft.com/d15d5a3f-6b38-4b92-b59c-ff0d27d111d9">SID_AND_ATTRIBUTES</a> structure.

This parameter can be <b>NULL</b> if no SIDs are to be disabled.


### -param DeletePrivilegeCount [in]

Specifies the number of entries in the <i>PrivilegesToDelete</i> array.


### -param PrivilegesToDelete [in, optional]

A pointer to an array of 
<a href="https://msdn.microsoft.com/f337b561-4b67-42a0-b8de-06f546bafb26">LUID_AND_ATTRIBUTES</a> structures that specify the privileges to delete in the restricted token. 




The <a href="https://msdn.microsoft.com/e94de19c-de12-40fb-a72c-060f7ad12f75">GetTokenInformation</a> function can be used with the TokenPrivileges flag to retrieve the privileges held by the existing token. The function ignores any privileges in the array that are not held by the existing token.

The function ignores the <b>Attributes</b> members of the <a href="https://msdn.microsoft.com/f337b561-4b67-42a0-b8de-06f546bafb26">LUID_AND_ATTRIBUTES</a> structures.

This parameter can be <b>NULL</b> if you do not want to delete any privileges.

If the calling program passes too many privileges in this array, <b>CreateRestrictedToken</b> returns ERROR_INVALID_PARAMETER.


### -param RestrictedSidCount [in]

Specifies the number of entries in the <i>SidsToRestrict</i> array.


### -param SidsToRestrict [in, optional]

A pointer to an array of 
<a href="https://msdn.microsoft.com/d15d5a3f-6b38-4b92-b59c-ff0d27d111d9">SID_AND_ATTRIBUTES</a> structures that specify a list of restricting SIDs for the new token. If the existing token is a restricted token, the list of restricting SIDs for the new token is the intersection of this array and the list of restricting SIDs for the existing token. No check is performed to remove duplicate SIDs that were placed on the <i>SidsToRestrict</i> parameter. Duplicate SIDs allow a restricted token to have redundant information in the restricting SID list. 




The <b>Attributes</b> member of the <a href="https://msdn.microsoft.com/d15d5a3f-6b38-4b92-b59c-ff0d27d111d9">SID_AND_ATTRIBUTES</a> structure must be zero. Restricting SIDs are always enabled for access checks.

This parameter can be <b>NULL</b> if you do not want to specify any restricting SIDs.


### -param NewTokenHandle [out]

A pointer to a variable that receives a handle to the new restricted token. This handle has the same access rights as <i>ExistingTokenHandle</i>. The new token is the same type, <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">primary</a> or <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">impersonation</a>, as the existing token. The handle returned in <i>NewTokenHandle</i> can be duplicated.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>CreateRestrictedToken</b> function can restrict the token in the following ways:

<ul>
<li>Apply the deny-only attribute to SIDs in the token so they cannot be used to access secured objects. For more information about the deny-only attribute, see 
<a href="https://msdn.microsoft.com/c902f876-f05e-4b0c-ab65-a0c6cebca933">SID Attributes in an Access Token</a>.</li>
<li>Remove 
<a href="https://msdn.microsoft.com/fe6aae0f-93eb-4aba-a6ac-45e71c251c51">privileges</a> from the token.</li>
<li>Specify a list of restricting SIDs, which the system uses when it checks the token's access to a securable object. The system performs two access checks: one using the token's enabled SIDs, and another using the list of restricting SIDs. Access is granted only if both access checks allow the requested access rights.</li>
</ul>
You can use the restricted token in the 
<a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a> function to create a process that has restricted access rights and privileges. If a process calls <b>CreateProcessAsUser</b> using a restricted version of its own token, the calling process does not need to have the SE_ASSIGNPRIMARYTOKEN_NAME privilege.

You can use the restricted token in the 
<a href="https://msdn.microsoft.com/cf5c31ae-6749-45c2-888f-697060cc8c75">ImpersonateLoggedOnUser</a> function.

<div class="alert"><b>Caution</b>  Applications that use restricted tokens should run the restricted application on desktops other than the default desktop. This is necessary to prevent an attack by a restricted application, using <b>SendMessage</b> or <b>PostMessage</b>, to unrestricted applications on the default desktop. If necessary, switch between desktops for your application purposes.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a>



<a href="https://msdn.microsoft.com/e94de19c-de12-40fb-a72c-060f7ad12f75">GetTokenInformation</a>



<a href="https://msdn.microsoft.com/cf5c31ae-6749-45c2-888f-697060cc8c75">ImpersonateLoggedOnUser</a>



<a href="https://msdn.microsoft.com/eaa63bb9-3084-4246-b2ab-f913bb7348fb">IsTokenRestricted</a>



<a href="https://msdn.microsoft.com/f337b561-4b67-42a0-b8de-06f546bafb26">LUID_AND_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/d15d5a3f-6b38-4b92-b59c-ff0d27d111d9">SID_AND_ATTRIBUTES</a>
 

 

