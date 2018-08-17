---
UID: NF:winreg.RegGetKeySecurity
title: RegGetKeySecurity function
author: windows-sdk-content
description: Retrieves a copy of the security descriptor protecting the specified open registry key.
old-location: security\reggetkeysecurity.htm
old-project: secauthz
ms.assetid: 26bd8f89-9241-4c13-a214-c2b276d68c92
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: RegGetKeySecurity, RegGetKeySecurity function [Security], _win32_reggetkeysecurity, security.reggetkeysecurity, winreg/RegGetKeySecurity
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winreg.h
req.include-header: Windows.h
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
req.typenames: PERF_OBJECT_TYPE, *PPERF_OBJECT_TYPE
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
 - RegGetKeySecurity
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RegGetKeySecurity function


## -description


The <b>RegGetKeySecurity</b> function retrieves a copy of the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> protecting the specified open registry key.


## -parameters




### -param hKey [in]

A handle to an open key for which to retrieve the security descriptor.


### -param SecurityInformation [in]

A 
<a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a> value that indicates the requested security information.


### -param pSecurityDescriptor [out, optional]

A pointer to a buffer that receives a copy of the requested security descriptor.


### -param lpcbSecurityDescriptor [in, out]

A pointer to a variable that specifies the size, in bytes, of the buffer pointed to by the <i>pSecurityDescriptor</i> parameter. When the function returns, the variable contains the number of bytes written to the buffer.


## -returns



If the function succeeds, the function returns ERROR_SUCCESS.
						

If the function fails, it returns a nonzero error code defined in WinError.h. You can use the 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.




## -remarks



If the buffer specified by the <i>pSecurityDescriptor</i> parameter is too small, the function returns ERROR_INSUFFICIENT_BUFFER and the <i>lpcbSecurityDescriptor</i> parameter contains the number of bytes required for the requested security descriptor.

To read the owner, group, or <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a> (DACL) from the key's security descriptor, the calling <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">process</a> must have been granted READ_CONTROL access when the handle was opened. To get READ_CONTROL access, the caller must be the owner of the key or the key's DACL must grant the access.

To read the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL) from the security descriptor, the calling process must have been granted ACCESS_SYSTEM_SECURITY access when the key was opened. The correct way to get this access is to enable the SE_SECURITY_NAME privilege in the caller's current token, open the handle for ACCESS_SYSTEM_SECURITY access, and then disable the privilege.




## -see-also




<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a>



<a href="https://msdn.microsoft.com/16337b77-23c5-4b7a-a344-66a02ee0e8a8">Low-level Access Control</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Low-level Access Control Functions</a>



<a href="https://msdn.microsoft.com/a2310ca0-1b9f-48d1-a3b5-ea3a528bfaba">RegDeleteKey</a>



<a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a>



<a href="https://msdn.microsoft.com/08bf8fc1-6a08-490e-b589-730211774257">RegSetKeySecurity</a>



<a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a>
 

 

