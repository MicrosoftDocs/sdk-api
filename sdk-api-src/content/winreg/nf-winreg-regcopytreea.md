---
UID: NF:winreg.RegCopyTreeA
title: RegCopyTreeA function (winreg.h)
author: windows-sdk-content
description: Copies the specified registry key, along with its values and subkeys, to the specified destination key.
old-location: base\regcopytree.htm
tech.root: SysInfo
ms.assetid: d16f2b47-e537-42b0-90b3-9f9a00e61e76
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RegCopyTree, RegCopyTree function, RegCopyTreeA, RegCopyTreeW, base.regcopytree, winreg/RegCopyTree, winreg/RegCopyTreeA, winreg/RegCopyTreeW
ms.topic: function
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegCopyTreeW (Unicode) and RegCopyTreeA (ANSI)
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
 - API-MS-Win-Core-registry-l2-1-0.dll
 - advapi32legacy.dll
 - API-MS-Win-Core-Registry-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - MinKernelBase.dll
 - api-ms-win-core-registry-l1-1-1.dll
 - api-ms-win-core-registry-l2-2-0.dll
api_name:
 - RegCopyTree
 - RegCopyTreeA
 - RegCopyTreeW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RegCopyTreeA function


## -description


Copies the specified registry key, along with its values and subkeys, to the specified destination key.


## -parameters




### -param hKeySrc [in]

A handle to an open registry key. The key must have been opened with the KEY_READ access right. For more information, see 
<a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>. 




This handle is returned by the 
<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a> or 
<a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a> function, or it can be one of the <a href="https://msdn.microsoft.com/db747656-b414-4594-ad39-6b476799060c">predefined keys</a>.


### -param lpSubKey [in, optional]

The name of the key. This key must be a subkey of the key identified by the <i>hKeySrc</i> parameter. This parameter can also be <b>NULL</b>.


### -param hKeyDest [in]

A handle to the destination key. The calling process  must have KEY_CREATE_SUB_KEY access to the key.  




This handle is returned by the 
<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a> or 
<a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a> function, or it can be one of the <a href="https://msdn.microsoft.com/db747656-b414-4594-ad39-6b476799060c">predefined keys</a>.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.




## -remarks



This function also copies the security descriptor for the key.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>
 

 

