---
UID: NF:securityappcontainer.GetAppContainerNamedObjectPath
title: GetAppContainerNamedObjectPath function (securityappcontainer.h)
description: Retrieves the named object path for the app container.
helpviewer_keywords: ["GetAppContainerNamedObjectPath","GetAppContainerNamedObjectPath function [Security]","security.getappcontainernamedobjectpath","securityappcontainer/GetAppContainerNamedObjectPath"]
old-location: security\getappcontainernamedobjectpath.htm
tech.root: security
ms.assetid: 466CE2DA-332E-4AA7-A0EB-868A646C0979
ms.date: 12/05/2018
ms.keywords: GetAppContainerNamedObjectPath, GetAppContainerNamedObjectPath function [Security], security.getappcontainernamedobjectpath, securityappcontainer/GetAppContainerNamedObjectPath
req.header: securityappcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetAppContainerNamedObjectPath
 - securityappcontainer/GetAppContainerNamedObjectPath
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Security-AppContainer-l1-1-0.dll
 - KernelBase.dll
api_name:
 - GetAppContainerNamedObjectPath
---

# GetAppContainerNamedObjectPath function


## -description

The <b>GetAppContainerNamedObjectPath</b> function retrieves the named object path for the app container. Each app container has its own named object path.

## -parameters

### -param Token [in, optional]

A handle pertaining to the token. If <b>NULL</b> is passed in and no <i>AppContainerSid</i> parameter is passed in, the caller's current process token is used, or the thread token if impersonating.

### -param AppContainerSid [in, optional]

The SID of the app container.

### -param ObjectPathLength [in]

The length of the buffer.

### -param ObjectPath [out, optional]

Buffer that is filled with the named object path.

### -param ReturnLength [out]

Returns the length required to accommodate the length of the named object path.

## -returns

If the function succeeds, the function returns a value of <b>TRUE</b>. 

If the function fails, it returns a value of <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

For assistive technology tools that work across Windows Store apps and desktop applications and have features that get loaded in the context of Windows Store apps, at times it may be necessary for the in-context feature to synchronize with the tool. Typically such synchronization is accomplished by establishing a named object in the user's session. Windows Store apps pose a challenge for this mechanism because, by default, named objects in the user's or global session are not accessible to Windows Store apps. We recommend that you update assistive technology tools to use <a href="/windows/desktop/AppUIStart/user-interface-technologies-for-windows-applications">UI Automation APIs</a> or <a href="/previous-versions/windows/desktop/magapi/entry-magapi-sdk">Magnification APIs</a> to avoid such pitfalls. In the interim, it may be necessary to continue using named objects.


#### Examples

The following sample established a named object so that it is accessible from a Windows Store app.


```cpp
#pragma comment(lib, "advapi32.lib")
#include <windows.h>
#include <stdio.h>
#include <aclapi.h>
#include <tchar.h>

int main(void)
{
BOOL GetLogonSid (HANDLE hToken, PSID *ppsid) 
{
    BOOL bSuccess = FALSE;
    DWORD dwLength = 0;
    PTOKEN_GROUPS ptg = NULL;

    // Verify the parameter passed in is not NULL.
    if (NULL == ppsid)
        goto Cleanup;

    // Get required buffer size and allocate the TOKEN_GROUPS buffer.

    if (!GetTokenInformation(
            hToken,         // handle to the access token
            TokenLogonSid,    // get information about the token's groups 
            (LPVOID) ptg,   // pointer to TOKEN_GROUPS buffer
            0,              // size of buffer
            &dwLength       // receives required buffer size
        )) 
    {
        if (GetLastError() != ERROR_INSUFFICIENT_BUFFER) 
            goto Cleanup;

        ptg = (PTOKEN_GROUPS)HeapAlloc(GetProcessHeap(),
                                    HEAP_ZERO_MEMORY, dwLength);

        if (ptg == NULL)
            goto Cleanup;
    }

    // Get the token group information from the access token.

    if (!GetTokenInformation(
            hToken,         // handle to the access token
            TokenLogonSid,    // get information about the token's groups 
            (LPVOID) ptg,   // pointer to TOKEN_GROUPS buffer
            dwLength,       // size of buffer
            &dwLength       // receives required buffer size
            ) || ptg->GroupCount != 1) 
    {
        goto Cleanup;
    }

    // Found the logon SID; make a copy of it.

    dwLength = GetLengthSid(ptg->Groups[0].Sid);
    *ppsid = (PSID) HeapAlloc(GetProcessHeap(),
                HEAP_ZERO_MEMORY, dwLength);
    if (*ppsid == NULL)
        goto Cleanup;
    if (!CopySid(dwLength, *ppsid, ptg->Groups[0].Sid)) 
    {
        HeapFree(GetProcessHeap(), 0, (LPVOID)*ppsid);
        goto Cleanup;
    }

   bSuccess = TRUE;

Cleanup: 

    // Free the buffer for the token groups.

    if (ptg != NULL)
        HeapFree(GetProcessHeap(), 0, (LPVOID)ptg);

    return bSuccess;
}

BOOL
CreateObjectSecurityDescriptor(PSID pLogonSid, PSECURITY_DESCRIPTOR* ppSD)
{
    BOOL bSuccess = FALSE;
    DWORD dwRes;
    PSID pAllAppsSID = NULL;
    PACL pACL = NULL;
    PSECURITY_DESCRIPTOR pSD = NULL;
    EXPLICIT_ACCESS ea[2];
    SID_IDENTIFIER_AUTHORITY ApplicationAuthority = SECURITY_APP_PACKAGE_AUTHORITY;

    // Create a well-known SID for the all appcontainers group.
    if(!AllocateAndInitializeSid(&ApplicationAuthority, 
            SECURITY_BUILTIN_APP_PACKAGE_RID_COUNT,
            SECURITY_APP_PACKAGE_BASE_RID,
            SECURITY_BUILTIN_PACKAGE_ANY_PACKAGE,
            0, 0, 0, 0, 0, 0,
            &pAllAppsSID))
    {
        wprintf(L"AllocateAndInitializeSid Error %u\n", GetLastError());
        goto Cleanup;
    }

    // Initialize an EXPLICIT_ACCESS structure for an ACE.
    // The ACE will allow LogonSid generic all access
    ZeroMemory(&ea, 2 * sizeof(EXPLICIT_ACCESS));
    ea[0].grfAccessPermissions = STANDARD_RIGHTS_ALL | MUTEX_ALL_ACCESS;
    ea[0].grfAccessMode = SET_ACCESS;
    ea[0].grfInheritance= NO_INHERITANCE;
    ea[0].Trustee.TrusteeForm = TRUSTEE_IS_SID;
    ea[0].Trustee.TrusteeType = TRUSTEE_IS_USER;
    ea[0].Trustee.ptstrName  = (LPTSTR) pLogonSid;

    // Initialize an EXPLICIT_ACCESS structure for an ACE.
    // The ACE will allow the all appcontainers execute permission
    ea[1].grfAccessPermissions = STANDARD_RIGHTS_READ | STANDARD_RIGHTS_EXECUTE | SYNCHRONIZE | MUTEX_MODIFY_STATE;
    ea[1].grfAccessMode = SET_ACCESS;
    ea[1].grfInheritance= NO_INHERITANCE;
    ea[1].Trustee.TrusteeForm = TRUSTEE_IS_SID;
    ea[1].Trustee.TrusteeType = TRUSTEE_IS_GROUP;
    ea[1].Trustee.ptstrName  = (LPTSTR) pAllAppsSID;

    // Create a new ACL that contains the new ACEs.
    dwRes = SetEntriesInAcl(2, ea, NULL, &pACL);
    if (ERROR_SUCCESS != dwRes) 
    {
        wprintf(L"SetEntriesInAcl Error %u\n", GetLastError());
        goto Cleanup;
    }

    // Initialize a security descriptor.  
    pSD = (PSECURITY_DESCRIPTOR) LocalAlloc(LPTR, 
                             SECURITY_DESCRIPTOR_MIN_LENGTH); 
    if (NULL == pSD) 
    { 
        wprintf(L"LocalAlloc Error %u\n", GetLastError());
        goto Cleanup; 
    } 
 
    if (!InitializeSecurityDescriptor(pSD,
            SECURITY_DESCRIPTOR_REVISION)) 
    {  
        wprintf(L"InitializeSecurityDescriptor Error %u\n",
                                GetLastError());
        goto Cleanup; 
    } 
 
    // Add the ACL to the security descriptor. 
    if (!SetSecurityDescriptorDacl(pSD, 
            TRUE,     // bDaclPresent flag   
            pACL, 
            FALSE))   // not a default DACL 
    {  
        wprintf(L"SetSecurityDescriptorDacl Error %u\n",
                GetLastError());
        goto Cleanup; 
    } 

    *ppSD = pSD;
    pSD = NULL;
    bSuccess = TRUE;
Cleanup:

    if (pAllAppsSID) 
        FreeSid(pAllAppsSID);
    if (pACL) 
        LocalFree(pACL);
    if (pSD) 
        LocalFree(pSD);

    return bSuccess;
}

    PSID pLogonSid = NULL;
    PSECURITY_DESCRIPTOR pSd = NULL;
    SECURITY_ATTRIBUTES  SecurityAttributes;
    HANDLE hToken = NULL;
    HANDLE hMutex = NULL;

    //Allowing LogonSid and all appcontainers. 
    if (GetLogonSid(hToken, &pLogonSid) && CreateObjectSecurityDescriptor(pLogonSid, &pSd) )
    {
        SecurityAttributes.nLength = sizeof(SECURITY_ATTRIBUTES);
        SecurityAttributes.bInheritHandle = TRUE;
        SecurityAttributes.lpSecurityDescriptor = pSd;

        hMutex = CreateMutex( 
                    &SecurityAttributes,         // default security descriptor
                    FALSE,                       // mutex not owned
                    TEXT("NameOfMutexObject"));  // object name
    }

    return 0;
}

```