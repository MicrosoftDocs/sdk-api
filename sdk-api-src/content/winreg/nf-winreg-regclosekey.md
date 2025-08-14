---
UID: NF:winreg.RegCloseKey
title: RegCloseKey function (winreg.h)
description: Closes a handle to the specified registry key.
helpviewer_keywords: ["RegCloseKey","RegCloseKey function","_win32_regclosekey","base.regclosekey","winreg/RegCloseKey"]
old-location: base\regclosekey.htm
tech.root: winprog
ms.assetid: 10175499-abf3-4694-9594-bb97b43f3fa5
ms.date: 12/05/2018
ms.keywords: RegCloseKey, RegCloseKey function, _win32_regclosekey, base.regclosekey, winreg/RegCloseKey
req.header: winreg.h
req.include-header: Windows.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegCloseKey
 - winreg/RegCloseKey
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
 - kernel32.dll
api_name:
 - RegCloseKey
---

# RegCloseKey function


## -description

Closes a handle to the specified registry key.

## -parameters

### -param hKey [in]

A handle to the open key to be closed. The handle must have been opened by the 
<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a>, 
<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeytransacteda">RegCreateKeyTransacted</a>, <a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a>, <a href="/windows/desktop/api/winreg/nf-winreg-regopenkeytransacteda">RegOpenKeyTransacted</a>, or <a href="/windows/desktop/api/winreg/nf-winreg-regconnectregistrya">RegConnectRegistry</a> function.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.

## -remarks

The handle for a specified key should not be used after it has been closed, because it will no longer be valid. Key handles should not be left open any longer than necessary.

The 
<b>RegCloseKey</b> function does not necessarily write information to the registry before returning; it can take as much as several seconds for the cache to be flushed to the hard disk. If an application must explicitly write registry information to the hard disk, it can use the 
<a href="/windows/desktop/api/winreg/nf-winreg-regflushkey">RegFlushKey</a> function. 
<b>RegFlushKey</b>, however, uses many system resources and should be called only when necessary.


#### Examples

For an example, see 
<a href="/windows/desktop/SysInfo/deleting-a-key-with-subkeys">Deleting a Key with Subkeys</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winreg/nf-winreg-regconnectregistrya">RegConnectRegistry</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regdeletekeya">RegDeleteKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regflushkey">RegFlushKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a>



<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>



<a href="/windows/desktop/SysInfo/registry">Registry Overview</a>