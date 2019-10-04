---
UID: NF:winreg.RegDisableReflectionKey
title: RegDisableReflectionKey function (winreg.h)
author: windows-sdk-content
description: Disables registry reflection for the specified key. Disabling reflection for a key does not affect reflection of any subkeys.
old-location: base\regdisablereflectionkey.htm
tech.root: SysInfo
ms.assetid: 294a1d28-d09f-44a3-8bc0-6fae50c3a8f8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RegDisableReflectionKey, RegDisableReflectionKey function, base.regdisablereflectionkey, winreg/RegDisableReflectionKey
ms.topic: function
f1_keywords: 
 - "winreg/RegDisableReflectionKey"
dev_langs:
 - c++
req.header: winreg.h
req.include-header: Windows.h
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
api_name:
 - RegDisableReflectionKey
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RegDisableReflectionKey function


## -description


Disables registry reflection for the specified key. Disabling reflection for a key does not affect reflection of any subkeys.


## -parameters




### -param hBase [in]

A handle to an open registry key. This handle is returned by the 
<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a>, <a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regcreatekeytransacteda">RegCreateKeyTransacted</a>, <a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a>, or 
<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regopenkeytransacteda">RegOpenKeyTransacted</a> function; it cannot specify a key on a remote computer.

If the key is not on the reflection list, the function succeeds but has no effect. For more information, see <a href="https://docs.microsoft.com/windows/desktop/WinProg64/registry-redirector">Registry Redirector</a>and <a href="https://docs.microsoft.com/windows/desktop/WinProg64/registry-reflection">Registry Reflection</a>.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.




## -remarks



On WOW64, 32-bit applications view a registry tree that is separate from the registry tree that 64-bit applications view. Registry reflection copies specific registry keys and values between the two views.

To restore registry reflection for a disabled key, use the <a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regenablereflectionkey">RegEnableReflectionKey</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regenablereflectionkey">RegEnableReflectionKey</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regqueryreflectionkey">RegQueryReflectionKey</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/registry-functions">Registry Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/WinProg64/registry-redirector">Registry Redirector</a>
 

 

