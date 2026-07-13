---
UID: NF:winreg.RegEnableReflectionKey
title: RegEnableReflectionKey function (winreg.h)
description: Restores registry reflection for the specified disabled key. Restoring reflection for a key does not affect reflection of any subkeys.
helpviewer_keywords: ["RegEnableReflectionKey","RegEnableReflectionKey function","base.regenablereflectionkey","winreg/RegEnableReflectionKey"]
old-location: base\regenablereflectionkey.htm
tech.root: winprog
ms.assetid: 6dfbc3d8-cd71-4ee9-a10b-955c26a6894c
ms.date: 12/05/2018
ms.keywords: RegEnableReflectionKey, RegEnableReflectionKey function, base.regenablereflectionkey, winreg/RegEnableReflectionKey
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegEnableReflectionKey
 - winreg/RegEnableReflectionKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - RegEnableReflectionKey
---

# RegEnableReflectionKey function


## -description

Restores registry reflection for the specified disabled key. Restoring reflection for a key does not affect reflection of any subkeys.

## -parameters

### -param hBase [in]

A handle to the registry key that was previously disabled using the <a href="/windows/desktop/api/winreg/nf-winreg-regdisablereflectionkey">RegDisableReflectionKey</a> function. This handle is returned by the 
<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a>, <a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeytransacteda">RegCreateKeyTransacted</a>, <a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a>, or 
<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeytransacteda">RegOpenKeyTransacted</a> function; it cannot specify a key on a remote computer.

If the key is not on the reflection list, this function succeeds but has no effect. For more information, see <a href="/windows/desktop/WinProg64/registry-redirector">Registry Redirector</a> and <a href="/windows/desktop/WinProg64/registry-reflection">Registry Reflection</a>.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.

## -remarks

On WOW64, 32-bit applications view a registry tree that is separate from the registry tree that 64-bit applications view. Registry reflection copies specific registry keys and values between the two views.

## -see-also

<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regdisablereflectionkey">RegDisableReflectionKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regqueryreflectionkey">RegQueryReflectionKey</a>



<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>



<a href="/windows/desktop/WinProg64/registry-redirector">Registry Redirector</a>