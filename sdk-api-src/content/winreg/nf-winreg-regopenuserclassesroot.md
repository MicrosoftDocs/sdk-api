---
UID: NF:winreg.RegOpenUserClassesRoot
title: RegOpenUserClassesRoot function (winreg.h)
description: Retrieves a handle to the HKEY_CLASSES_ROOT key for a specified user. The user is identified by an access token.
helpviewer_keywords: ["RegOpenUserClassesRoot","RegOpenUserClassesRoot function","_win32_regopenuserclassesroot","base.regopenuserclassesroot","winreg/RegOpenUserClassesRoot"]
old-location: base\regopenuserclassesroot.htm
tech.root: winprog
ms.assetid: bd068826-cf88-4fc7-a7d6-96cc03e923c7
ms.date: 12/05/2018
ms.keywords: RegOpenUserClassesRoot, RegOpenUserClassesRoot function, _win32_regopenuserclassesroot, base.regopenuserclassesroot, winreg/RegOpenUserClassesRoot
req.header: winreg.h
req.include-header: Windows.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegOpenUserClassesRoot
 - winreg/RegOpenUserClassesRoot
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-registry-l1-1-2.dll
 - Advapi32.dll
 - API-MS-Win-Core-Localregistry-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Registry-l1-1-0.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - MinKernelBase.dll
 - api-ms-win-core-registry-l1-1-1.dll
api_name:
 - RegOpenUserClassesRoot
---

# RegOpenUserClassesRoot function


## -description

Retrieves a handle to the <b>HKEY_CLASSES_ROOT</b> key for a specified user. The user is identified by an access token. The returned key has a view of the registry that merges the contents of the <b>HKEY_LOCAL_MACHINE</b>\Software\Classes key with the contents of the Software\Classes keys in the user's registry hive. For more information, see 
<a href="/windows/desktop/SysInfo/hkey-classes-root-key">HKEY_CLASSES_ROOT Key</a>.

## -parameters

### -param hToken [in]

A handle to a primary or impersonation access token that identifies the user of interest. This can be a token handle returned by a call to 
<a href="/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a>, 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken">CreateRestrictedToken</a>, 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-duplicatetoken">DuplicateToken</a>, 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex">DuplicateTokenEx</a>, 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocesstoken">OpenProcessToken</a>, or 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken">OpenThreadToken</a> functions. 




The handle must have TOKEN_QUERY access. For more information, see 
<a href="/windows/desktop/SecAuthZ/access-rights-for-access-token-objects">Access Rights for Access-Token Objects</a>.

### -param dwOptions

This parameter is reserved and must be zero.

### -param samDesired [in]

A mask that specifies the desired access rights to the key. The function fails if the security descriptor of the key does not permit the requested access for the calling process. For more information, see 
<a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>.

### -param phkResult [out]

A pointer to a variable that receives a handle to the opened key. When you no longer need the returned handle, call the 
<a href="/windows/desktop/api/winreg/nf-winreg-regclosekey">RegCloseKey</a> function to close it.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.

## -remarks

The 
<b>RegOpenUserClassesRoot</b> function enables you to retrieve the merged <b>HKEY_CLASSES_ROOT</b> information for users other than the interactive user. For example, the server component of a client/server application could use 
<b>RegOpenUserClassesRoot</b> to retrieve the merged information for a client.

<b>RegOpenUserClassesRoot</b> fails if the user profile for the specified user is not loaded. When a user logs on interactively, the system automatically loads the user's profile. For other users, you can call the 
<a href="/windows/desktop/api/userenv/nf-userenv-loaduserprofilea">LoadUserProfile</a> function to load the user's profile. However, <b>LoadUserProfile</b> can be very time-consuming, so do not call it for this purpose unless it is absolutely necessary to have the user's merged <b>HKEY_CLASSES_ROOT</b> information.

Applications running in the security context of the interactively logged-on user do not need to use 
<b>RegOpenUserClassesRoot</b>. These applications can call the 
<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a> function to retrieve a merged view of the <b>HKEY_CLASSES_ROOT</b> key for the interactive user.

## -see-also

<a href="/windows/desktop/api/userenv/nf-userenv-loaduserprofilea">LoadUserProfile</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regclosekey">RegCloseKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a>



<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>



<a href="/windows/desktop/SysInfo/registry">Registry Overview</a>