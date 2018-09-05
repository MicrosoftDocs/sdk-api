---
UID: NF:winreg.RegCloseKey
title: RegCloseKey function
author: windows-sdk-content
description: Closes a handle to the specified registry key.
old-location: base\regclosekey.htm
old-project: SysInfo
ms.assetid: 10175499-abf3-4694-9594-bb97b43f3fa5
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: RegCloseKey, RegCloseKey function, _win32_regclosekey, base.regclosekey, winreg/RegCloseKey
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winreg.h
req.include-header: Windows.h
req.redist: 
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
 - kernel32.dll
api_name:
 - RegCloseKey
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RegCloseKey function


## -description


Closes a handle to the specified registry key.


## -parameters




### -param hKey [in]

A handle to the open key to be closed. The handle must have been opened by the 
<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a>, 
<a href="https://msdn.microsoft.com/f18e5ff9-41c3-4c26-8d01-a8ec69bcdef2">RegCreateKeyTransacted</a>, <a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a>, <a href="https://msdn.microsoft.com/11663ed2-d17c-4f08-be7b-9b591271fbcd">RegOpenKeyTransacted</a>, or <a href="https://msdn.microsoft.com/d7fb41cc-4855-4ad7-879c-b1ac85ac5803">RegConnectRegistry</a> function.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.




## -remarks



The handle for a specified key should not be used after it has been closed, because it will no longer be valid. Key handles should not be left open any longer than necessary.

The 
<b>RegCloseKey</b> function does not necessarily write information to the registry before returning; it can take as much as several seconds for the cache to be flushed to the hard disk. If an application must explicitly write registry information to the hard disk, it can use the 
<a href="https://msdn.microsoft.com/ae1160be-1da7-4621-a0fc-727aa229ec06">RegFlushKey</a> function. 
<b>RegFlushKey</b>, however, uses many system resources and should be called only when necessary.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/1cf6db95-85a4-4416-b17e-e14f45804503">Deleting a Key with Subkeys</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/d7fb41cc-4855-4ad7-879c-b1ac85ac5803">RegConnectRegistry</a>



<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a>



<a href="https://msdn.microsoft.com/a2310ca0-1b9f-48d1-a3b5-ea3a528bfaba">RegDeleteKey</a>



<a href="https://msdn.microsoft.com/ae1160be-1da7-4621-a0fc-727aa229ec06">RegFlushKey</a>



<a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>



<a href="https://msdn.microsoft.com/ffb06903-593e-47ce-adb2-baed5d379110">Registry Overview</a>
 

 

