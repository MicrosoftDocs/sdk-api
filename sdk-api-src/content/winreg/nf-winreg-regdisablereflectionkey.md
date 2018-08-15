---
UID: NF:winreg.RegDisableReflectionKey
title: RegDisableReflectionKey function
author: windows-sdk-content
description: Disables registry reflection for the specified key. Disabling reflection for a key does not affect reflection of any subkeys.
old-location: base\regdisablereflectionkey.htm
old-project: SysInfo
ms.assetid: 294a1d28-d09f-44a3-8bc0-6fae50c3a8f8
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: RegDisableReflectionKey, RegDisableReflectionKey function, base.regdisablereflectionkey, winreg/RegDisableReflectionKey
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winreg.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP Professional x64 Edition [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
api_name:
 - RegDisableReflectionKey
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RegDisableReflectionKey function


## -description


Disables registry reflection for the specified key. Disabling reflection for a key does not affect reflection of any subkeys.


## -parameters




### -param hBase [in]

A handle to an open registry key. This handle is returned by the 
<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a>, <a href="https://msdn.microsoft.com/f18e5ff9-41c3-4c26-8d01-a8ec69bcdef2">RegCreateKeyTransacted</a>, <a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a>, or 
<a href="https://msdn.microsoft.com/11663ed2-d17c-4f08-be7b-9b591271fbcd">RegOpenKeyTransacted</a> function; it cannot specify a key on a remote computer.

If the key is not on the reflection list, the function succeeds but has no effect. For more information, see <a href="https://msdn.microsoft.com/b3989f79-0439-485a-96c1-4f2227d48653">Registry Redirector</a>and <a href="https://msdn.microsoft.com/eac9038b-9f59-4ac7-8974-f94a4a62a257">Registry Reflection</a>.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.




## -remarks



On WOW64, 32-bit applications view a registry tree that is separate from the registry tree that 64-bit applications view. Registry reflection copies specific registry keys and values between the two views.

To restore registry reflection for a disabled key, use the <a href="https://msdn.microsoft.com/6dfbc3d8-cd71-4ee9-a10b-955c26a6894c">RegEnableReflectionKey</a> function.




## -see-also




<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a>



<a href="https://msdn.microsoft.com/6dfbc3d8-cd71-4ee9-a10b-955c26a6894c">RegEnableReflectionKey</a>



<a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a>



<a href="https://msdn.microsoft.com/d7516eab-dbcf-4ece-931e-d7bb2a983503">RegQueryReflectionKey</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>



<a href="https://msdn.microsoft.com/b3989f79-0439-485a-96c1-4f2227d48653">Registry Redirector</a>
 

 

