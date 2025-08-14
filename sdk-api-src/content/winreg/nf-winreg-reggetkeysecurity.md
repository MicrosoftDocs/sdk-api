---
UID: NF:winreg.RegGetKeySecurity
title: RegGetKeySecurity function (winreg.h)
description: Retrieves a copy of the security descriptor protecting the specified open registry key.
helpviewer_keywords: ["RegGetKeySecurity","RegGetKeySecurity function [Security]","_win32_reggetkeysecurity","security.reggetkeysecurity","winreg/RegGetKeySecurity"]
old-location: security\reggetkeysecurity.htm
tech.root: security
ms.assetid: 26bd8f89-9241-4c13-a214-c2b276d68c92
ms.date: 12/05/2018
ms.keywords: RegGetKeySecurity, RegGetKeySecurity function [Security], _win32_reggetkeysecurity, security.reggetkeysecurity, winreg/RegGetKeySecurity
req.header: winreg.h
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
 - RegGetKeySecurity
 - winreg/RegGetKeySecurity
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
 - RegGetKeySecurity
---

# RegGetKeySecurity function


## -description

The <b>RegGetKeySecurity</b> function retrieves a copy of the <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> protecting the specified open registry key.

## -parameters

### -param hKey [in]

A handle to an open key for which to retrieve the security descriptor.

### -param SecurityInformation [in]

A 
<a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a> value that indicates the requested security information.

### -param pSecurityDescriptor [out, optional]

A pointer to a buffer that receives a copy of the requested security descriptor.

### -param lpcbSecurityDescriptor [in, out]

A pointer to a variable that specifies the size, in bytes, of the buffer pointed to by the <i>pSecurityDescriptor</i> parameter. When the function returns, the variable contains the number of bytes written to the buffer.

## -returns

If the function succeeds, the function returns ERROR_SUCCESS.
						

If the function fails, it returns a nonzero error code defined in WinError.h. You can use the 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.

## -remarks

If the buffer specified by the <i>pSecurityDescriptor</i> parameter is too small, the function returns ERROR_INSUFFICIENT_BUFFER and the <i>lpcbSecurityDescriptor</i> parameter contains the number of bytes required for the requested security descriptor.

To read the owner, group, or <a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL) from the key's security descriptor, the calling <a href="/windows/desktop/SecGloss/p-gly">process</a> must have been granted READ_CONTROL access when the handle was opened. To get READ_CONTROL access, the caller must be the owner of the key or the key's DACL must grant the access.

To read the <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL) from the security descriptor, the calling process must have been granted ACCESS_SYSTEM_SECURITY access when the key was opened. The correct way to get this access is to enable the SE_SECURITY_NAME privilege in the caller's current token, open the handle for ACCESS_SYSTEM_SECURITY access, and then disable the privilege.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>



<a href="/windows/desktop/SecAuthZ/low-level-access-control">Low-level Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Low-level Access Control Functions</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regdeletekeya">RegDeleteKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regsetkeysecurity">RegSetKeySecurity</a>



<a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a>