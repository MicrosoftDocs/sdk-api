---
UID: NF:winreg.RegQueryReflectionKey
title: RegQueryReflectionKey function (winreg.h)
description: Determines whether reflection has been disabled or enabled for the specified key.
helpviewer_keywords: ["RegQueryReflectionKey","RegQueryReflectionKey function","base.regqueryreflectionkey","winreg/RegQueryReflectionKey"]
old-location: base\regqueryreflectionkey.htm
tech.root: winprog
ms.assetid: d7516eab-dbcf-4ece-931e-d7bb2a983503
ms.date: 12/05/2018
ms.keywords: RegQueryReflectionKey, RegQueryReflectionKey function, base.regqueryreflectionkey, winreg/RegQueryReflectionKey
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
req.lib: AdvApi32.lib
req.dll: AdvApi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegQueryReflectionKey
 - winreg/RegQueryReflectionKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - AdvApi32.dll
api_name:
 - RegQueryReflectionKey
---

# RegQueryReflectionKey function


## -description

Determines whether reflection has been disabled or enabled for the specified key.

## -parameters

### -param hBase [in]

A handle to the registry key.
      This handle is returned by the 
<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a>, <a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeytransacteda">RegCreateKeyTransacted</a>, <a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a>, or 
<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeytransacteda">RegOpenKeyTransacted</a> function; it cannot specify a key on a remote computer.

### -param bIsReflectionDisabled [out]

A value that indicates whether reflection has been disabled through <a href="/windows/desktop/api/winreg/nf-winreg-regdisablereflectionkey">RegDisableReflectionKey</a> or enabled through <a href="/windows/desktop/api/winreg/nf-winreg-regenablereflectionkey">RegEnableReflectionKey</a>.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
       <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the
       FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.

## -remarks

On WOW64, 32-bit applications view a registry tree that is separate from the registry tree that 64-bit 
    applications view. Registry reflection copies specific registry keys and values between the two views.

To disable registry reflection, use the 
    <a href="/windows/desktop/api/winreg/nf-winreg-regdisablereflectionkey">RegDisableReflectionKey</a> function. To restore 
    reflection for a disabled key, use the 
    <a href="/windows/desktop/api/winreg/nf-winreg-regenablereflectionkey">RegEnableReflectionKey</a> function.

## -see-also

<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regdisablereflectionkey">RegDisableReflectionKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regenablereflectionkey">RegEnableReflectionKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a>



<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>



<a href="/windows/desktop/WinProg64/registry-redirector">Registry Redirector</a>