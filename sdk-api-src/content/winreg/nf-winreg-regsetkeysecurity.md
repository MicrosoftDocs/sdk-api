---
UID: NF:winreg.RegSetKeySecurity
title: RegSetKeySecurity function (winreg.h)
author: windows-sdk-content
description: Sets the security of an open registry key.
old-location: security\regsetkeysecurity.htm
tech.root: SecAuthZ
ms.assetid: 08bf8fc1-6a08-490e-b589-730211774257
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RegSetKeySecurity, RegSetKeySecurity function [Security], _win32_regsetkeysecurity, security.regsetkeysecurity, winreg/RegSetKeySecurity
ms.topic: function
f1_keywords: 
 - "winreg/RegSetKeySecurity"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-Core-Localregistry-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Registry-l1-1-0.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - MinKernelBase.dll
 - api-ms-win-core-registry-l1-1-1.dll
api_name:
 - RegSetKeySecurity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RegSetKeySecurity function


## -description


The <b>RegSetKeySecurity</b> function sets the security of an open registry key.


## -parameters




### -param hKey [in]

A handle to an open key for which the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security descriptor</a> is set.


### -param SecurityInformation [in]

A set of 
bit flags that indicate the type of security information to set. This parameter can be a combination of the 
<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a> bit flags.


### -param pSecurityDescriptor [in]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_security_descriptor">SECURITY_DESCRIPTOR</a> structure that specifies the security <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">attributes</a> to set for the specified key.


## -returns



If the function succeeds, the function returns ERROR_SUCCESS.
						

If the function fails, it returns a nonzero error code defined in WinError.h. You can use the 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.




## -remarks



If <i>hKey</i> is one of the predefined keys, use  the <a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regclosekey">RegCloseKey</a> function to close the predefined key to  ensure that the new security information is in effect the next time the predefined key is referenced.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/low-level-access-control">Low-level Access Control</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/authorization-functions">Low-level Access Control Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regclosekey">RegCloseKey</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regdeletekeya">RegDeleteKey</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-reggetkeysecurity">RegGetKeySecurity</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a>
 

 

