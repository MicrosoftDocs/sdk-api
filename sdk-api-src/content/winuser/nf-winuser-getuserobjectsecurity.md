---
UID: NF:winuser.GetUserObjectSecurity
title: GetUserObjectSecurity function (winuser.h)
description: Retrieves security information for the specified user object.
helpviewer_keywords: ["GetUserObjectSecurity","GetUserObjectSecurity function [Security]","_win32_getuserobjectsecurity","security.getuserobjectsecurity","winuser/GetUserObjectSecurity"]
old-location: security\getuserobjectsecurity.htm
tech.root: security
ms.assetid: 998c2520-7833-4efd-a794-b13b528f0485
ms.date: 12/05/2018
ms.keywords: GetUserObjectSecurity, GetUserObjectSecurity function [Security], _win32_getuserobjectsecurity, security.getuserobjectsecurity, winuser/GetUserObjectSecurity
req.header: winuser.h
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetUserObjectSecurity
 - winuser/GetUserObjectSecurity
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-usersecurity-l1-1-0.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Misc-l1-1-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - GetUserObjectSecurity
---

# GetUserObjectSecurity function


## -description

The <b>GetUserObjectSecurity</b> function retrieves security information for the specified user object.

## -parameters

### -param hObj [in]

A handle to the user object for which to return security information.

### -param pSIRequested [in]

A pointer to a 
<a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a> value that specifies the security information being requested.

### -param pSID [in, out, optional]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure in <a href="/windows/desktop/SecGloss/s-gly">self-relative</a> format that contains the requested information when the function returns. This buffer must be aligned on a 4-byte boundary.

### -param nLength [in]

The length, in bytes, of the buffer pointed to by the <i>pSD</i> parameter.

### -param lpnLengthNeeded [out]

A pointer to a variable to receive the number of bytes required to store the complete <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a>. If this variable's value is greater than the value of the <i>nLength</i> parameter when the function returns, the function returns <b>FALSE</b> and none of the security descriptor is copied to the buffer. Otherwise, the entire security descriptor is copied.

## -returns

If the function succeeds, the function returns nonzero.
						

If the function fails, it returns zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To read the owner, group, or <a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL) from the user object's security descriptor, the calling <a href="/windows/desktop/SecGloss/p-gly">process</a> must have been granted READ_CONTROL access when the handle was opened.

To read the <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL) from the security descriptor, the calling process must have been granted ACCESS_SYSTEM_SECURITY access when the handle was opened. The correct way to get this access is to enable the SE_SECURITY_NAME privilege in the caller's current token, open the handle for ACCESS_SYSTEM_SECURITY access, and then disable the privilege.


#### Examples

For an example that uses this function, see <a href="/previous-versions/aa379608(v=vs.85)">Starting an Interactive Client Process</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity">CreatePrivateObjectSecurity</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity">GetKernelObjectSecurity</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity">GetPrivateObjectSecurity</a>



<a href="/windows/desktop/SecAuthZ/low-level-access-control">Low-level Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Low-level Access Control Functions</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setuserobjectsecurity">SetUserObjectSecurity</a>