---
UID: NF:winreg.RegSetKeySecurity
title: RegSetKeySecurity function
author: windows-sdk-content
description: Sets the security of an open registry key.
old-location: security\regsetkeysecurity.htm
old-project: SecAuthZ
ms.assetid: 08bf8fc1-6a08-490e-b589-730211774257
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: RegSetKeySecurity, RegSetKeySecurity function [Security], _win32_regsetkeysecurity, security.regsetkeysecurity, winreg/RegSetKeySecurity
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: PERF_OBJECT_TYPE, *PPERF_OBJECT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Advapi32.dll
-	API-MS-Win-Core-Localregistry-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-Registry-l1-1-0.dll
-	API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
-	API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
-	MinKernelBase.dll
-	api-ms-win-core-registry-l1-1-1.dll
api_name:
-	RegSetKeySecurity
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RegSetKeySecurity function


## -description


The <b>RegSetKeySecurity</b> function sets the security of an open registry key.


## -parameters




### -param hKey [in]

A handle to an open key for which the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> is set.


### -param SecurityInformation [in]

A set of 
bit flags that indicate the type of security information to set. This parameter can be a combination of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556635">SECURITY_INFORMATION</a> bit flags.


### -param pSecurityDescriptor [in]

A pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> structure that specifies the security <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">attributes</a> to set for the specified key.


## -returns




						If the function succeeds, the function returns ERROR_SUCCESS.
						

If the function fails, it returns a nonzero error code defined in WinError.h. You can use the 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.




## -remarks



If <i>hKey</i> is one of the predefined keys, use  the <a href="https://msdn.microsoft.com/10175499-abf3-4694-9594-bb97b43f3fa5">RegCloseKey</a> function to close the predefined key to  ensure that the new security information is in effect the next time the predefined key is referenced.




## -see-also




<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a>



<a href="https://msdn.microsoft.com/16337b77-23c5-4b7a-a344-66a02ee0e8a8">Low-level Access Control</a>



<a href="authorization_functions.htm">Low-level Access Control Functions</a>



<a href="https://msdn.microsoft.com/10175499-abf3-4694-9594-bb97b43f3fa5">RegCloseKey</a>



<a href="https://msdn.microsoft.com/a2310ca0-1b9f-48d1-a3b5-ea3a528bfaba">RegDeleteKey</a>



<a href="https://msdn.microsoft.com/26bd8f89-9241-4c13-a214-c2b276d68c92">RegGetKeySecurity</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556635">SECURITY_INFORMATION</a>
 

 

