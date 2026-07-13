---
UID: NF:securitybaseapi.CreateRestrictedToken
title: CreateRestrictedToken function (securitybaseapi.h)
description: Creates a new access token that is a restricted version of an existing access token. The restricted token can have disabled security identifiers (SIDs), deleted privileges, and a list of restricting SIDs.
helpviewer_keywords: ["CreateRestrictedToken","CreateRestrictedToken function [Security]","DISABLE_MAX_PRIVILEGE","LUA_TOKEN","SANDBOX_INERT","WRITE_RESTRICTED","_win32_createrestrictedtoken","security.createrestrictedtoken","securitybaseapi/CreateRestrictedToken"]
old-location: security\createrestrictedtoken.htm
tech.root: security
ms.assetid: e087f360-5d1d-4846-b3d6-214a426e5222
ms.date: 12/05/2018
ms.keywords: CreateRestrictedToken, CreateRestrictedToken function [Security], DISABLE_MAX_PRIVILEGE, LUA_TOKEN, SANDBOX_INERT, WRITE_RESTRICTED, _win32_createrestrictedtoken, security.createrestrictedtoken, securitybaseapi/CreateRestrictedToken
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateRestrictedToken
 - securitybaseapi/CreateRestrictedToken
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-base-l1-2-2.dll
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
---

# CreateRestrictedToken function

## -description

The **CreateRestrictedToken** function creates a new [access token](/windows/win32/SecGloss/a-gly) that is a restricted version of an existing access token. The restricted token can have disabled [security identifiers](/windows/win32/SecGloss/s-gly) (SIDs), deleted privileges, and a list of restricting SIDs. For more information, see [Restricted Tokens](/windows/win32/SecAuthZ/restricted-tokens).

## -parameters

### -param ExistingTokenHandle [in]

A handle to a [primary](/windows/win32/SecGloss/p-gly) or [impersonation token](/windows/win32/SecGloss/i-gly). The token can also be a restricted token. The handle must have **TOKEN_DUPLICATE** access to the token.

### -param Flags [in]

Specifies additional privilege options. This parameter can be zero or a combination of the following values.

| Value | Meaning |
|-------|---------|
| **DISABLE_MAX_PRIVILEGE**<br/>`0x1` | Disables all privileges in the new token except the **SeChangeNotifyPrivilege** privilege. If this value is specified, the **DeletePrivilegeCount** and **PrivilegesToDelete** parameters are ignored. |
| **SANDBOX_INERT**<br/>`0x2` | If this value is used, the system does not check [AppLocker](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd723678(v=ws.10)) rules or apply [Software Restriction Policies](/previous-versions/windows/it-pro/windows-server-2003/cc779607(v=ws.10)). For [AppLocker](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd723678(v=ws.10)), this flag disables checks for all four rule collections: Executable, Windows Installer, Script, and DLL.<br/><br/>When creating a setup program that must run extracted DLLs during installation, use the flag **SAFER_TOKEN_MAKE_INERT** in the [SaferComputeTokenFromLevel](/windows/win32/api/winsafer/nf-winsafer-safercomputetokenfromlevel) function.<br/><br/>A token can be queried for existence of this flag by using [GetTokenInformation](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation).<br/><br/>**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** On systems with KB2532445 installed, the caller must be running as LocalSystem or TrustedInstaller or the system ignores this flag. For more information, see [You can circumvent AppLocker rules by using an Office macro on a computer that is running Windows 7 or Windows Server 2008 R2](https://support.microsoft.com/topic/you-can-circumvent-applocker-rules-by-using-an-office-macro-on-a-computer-that-is-running-windows-7-or-windows-server-2008-r2-b002ea09-1268-bb1f-f97b-d744103e220e).<br/><br/>**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** AppLocker is not supported. AppLocker was introduced in Windows 7 and Windows Server 2008 R2. |
| **LUA_TOKEN**<br/>`0x4` | The new token is a LUA token.<br/><br/>**Windows Server 2003 and Windows XP:** This value is not supported. |
| **WRITE_RESTRICTED**<br/>`0x8` | The new token contains restricting SIDs that are considered only when evaluating write access.<br/><br/>**Windows XP with SP2 and later:** The value of this constant is `0x4`. For an application to be compatible with Windows XP with SP2 and later operating systems, the application should query the operating system by calling the [GetVersionEx](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) function to determine which value should be used.<br/><br/>**Windows Server 2003 and Windows XP with SP1 and earlier:** This value is not supported. |

### -param DisableSidCount [in]

Specifies the number of entries in the *SidsToDisable* array.

### -param SidsToDisable [in, optional]

A pointer to an array of [SID_AND_ATTRIBUTES](/windows/win32/api/winnt/ns-winnt-sid_and_attributes) structures that specify the deny-only SIDs in the restricted token. The system uses a deny-only SID to deny access to a securable object. The absence of a deny-only SID does not allow access.

Disabling a SID turns on **SE_GROUP_USE_FOR_DENY_ONLY** and turns off **SE_GROUP_ENABLED** and **SE_GROUP_ENABLED_BY_DEFAULT**. All other attributes are ignored.

Deny-only attributes apply to any combination of an existing token's SIDs, including the user SID and group SIDs that have the SE_GROUP_MANDATORY attribute. To get the SIDs associated with the existing token, use the [GetTokenInformation](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) function with the TokenUser and TokenGroups flags. The function ignores any SIDs in the array that are not also found in the existing token.

The function ignores the **Attributes** member of the [SID_AND_ATTRIBUTES](/windows/win32/api/winnt/ns-winnt-sid_and_attributes) structure.

This parameter can be **NULL** if no SIDs are to be disabled.

### -param DeletePrivilegeCount [in]

Specifies the number of entries in the *PrivilegesToDelete* array.

### -param PrivilegesToDelete [in, optional]

A pointer to an array of [LUID_AND_ATTRIBUTES](/windows/win32/api/winnt/ns-winnt-luid_and_attributes) structures that specify the privileges to delete in the restricted token.

The [GetTokenInformation](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) function can be used with the TokenPrivileges flag to retrieve the privileges held by the existing token. The function ignores any privileges in the array that are not held by the existing token.

The function ignores the **Attributes** members of the [LUID_AND_ATTRIBUTES](/windows/win32/api/winnt/ns-winnt-luid_and_attributes) structures.

This parameter can be **NULL** if you do not want to delete any privileges.

If the calling program passes too many privileges in this array, **CreateRestrictedToken** returns **ERROR_INVALID_PARAMETER**.

### -param RestrictedSidCount [in]

Specifies the number of entries in the *SidsToRestrict* array.

### -param SidsToRestrict [in, optional]

A pointer to an array of [SID_AND_ATTRIBUTES](/windows/win32/api/winnt/ns-winnt-sid_and_attributes) structures that specify a list of restricting SIDs for the new token. If the existing token is a restricted token, the list of restricting SIDs for the new token is the intersection of this array and the list of restricting SIDs for the existing token. No check is performed to remove duplicate SIDs that were placed on the *SidsToRestrict* parameter. Duplicate SIDs allow a restricted token to have redundant information in the restricting SID list.

The **Attributes** member of the [SID_AND_ATTRIBUTES](/windows/win32/api/winnt/ns-winnt-sid_and_attributes) structure must be zero. Restricting SIDs are always enabled for access checks.

This parameter can be **NULL** if you do not want to specify any restricting SIDs.

### -param NewTokenHandle [out]

A pointer to a variable that receives a handle to the new restricted token. This handle has the same access rights as *ExistingTokenHandle*. The new token is the same type, [primary](/windows/win32/SecGloss/p-gly) or [impersonation](/windows/win32/SecGloss/i-gly), as the existing token. The handle returned in *NewTokenHandle* can be duplicated.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

The **CreateRestrictedToken** function can restrict the token in the following ways:

- Apply the deny-only attribute to SIDs in the token so they cannot be used to access secured objects. For more information about the deny-only attribute, see [SID Attributes in an Access Token](/windows/win32/SecAuthZ/sid-attributes-in-an-access-token).
- Remove [privileges](/windows/win32/SecAuthZ/privileges) from the token.
- Specify a list of restricting SIDs, which the system uses when it checks the token's access to a securable object. The system performs two access checks: one using the token's enabled SIDs, and another using the list of restricting SIDs. Access is granted only if both access checks allow the requested access rights.

You can use the restricted token in the [CreateProcessAsUser](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) function to create a process that has restricted access rights and privileges. If a process calls **CreateProcessAsUser** using a restricted version of its own token, the calling process does not need to have the **SE_ASSIGNPRIMARYTOKEN_NAME** privilege.

You can use the restricted token in the [ImpersonateLoggedOnUser](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) function.

> [!WARNING]
> Applications that use restricted tokens should run the restricted application on desktops other than the default desktop. This is necessary to prevent an attack by a restricted application, using **SendMessage** or **PostMessage**, to unrestricted applications on the default desktop. If necessary, switch between desktops for your application purposes.

## -see-also

[Access Control Overview](/windows/win32/SecAuthZ/access-control)

[Basic Access Control Functions](/windows/win32/SecAuthZ/authorization-functions)

[CreateProcessAsUser](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)

[GetTokenInformation](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation)

[ImpersonateLoggedOnUser](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser)

[IsTokenRestricted](/windows/win32/api/securitybaseapi/nf-securitybaseapi-istokenrestricted)

[LUID_AND_ATTRIBUTES](/windows/win32/api/winnt/ns-winnt-luid_and_attributes)

[SID_AND_ATTRIBUTES](/windows/win32/api/winnt/ns-winnt-sid_and_attributes)
