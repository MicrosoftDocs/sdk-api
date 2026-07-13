---
UID: NF:winreg.RegFlushKey
title: RegFlushKey function (winreg.h)
description: Writes all the attributes of the specified open registry key into the registry.
helpviewer_keywords: ["RegFlushKey","RegFlushKey function","_win32_regflushkey","base.regflushkey","winreg/RegFlushKey"]
old-location: base\regflushkey.htm
tech.root: winprog
ms.assetid: ae1160be-1da7-4621-a0fc-727aa229ec06
ms.date: 12/05/2018
ms.keywords: RegFlushKey, RegFlushKey function, _win32_regflushkey, base.regflushkey, winreg/RegFlushKey
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
 - RegFlushKey
 - winreg/RegFlushKey
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
api_name:
 - RegFlushKey
---

# RegFlushKey function


## -description

Writes all the attributes of the specified open registry key into the registry.

## -parameters

### -param hKey [in]

A handle to an open registry key. The key must have been opened with the KEY_QUERY_VALUE access right. For more information, see 
<a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>. 




This handle is returned by the 
<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a>, <a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeytransacteda">RegCreateKeyTransacted</a>, <a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a>, or 
<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeytransacteda">RegOpenKeyTransacted</a> function. It can also be one of the following 
<a href="/windows/desktop/SysInfo/predefined-keys">predefined keys</a>:<dl>
<dd><b>HKEY_CLASSES_ROOT</b></dd>
<dd><b>HKEY_CURRENT_CONFIG</b></dd>
<dd><b>HKEY_CURRENT_USER</b></dd>
<dd><b>HKEY_LOCAL_MACHINE</b></dd>
<dd><b>HKEY_PERFORMANCE_DATA</b></dd>
<dd><b>HKEY_USERS</b></dd>
</dl>

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.

## -remarks

Calling <b>RegFlushKey</b> is an expensive operation that significantly affects system-wide performance as  it consumes disk bandwidth and blocks modifications to all keys by all processes in the registry hive that is being flushed until the flush operation completes. <b>RegFlushKey</b> should only be called explicitly when an application must guarantee that registry changes are persisted to disk immediately after modification. All modifications made to keys are visible to other processes without the need to flush them to disk.

Alternatively, the registry has a 'lazy flush' mechanism that flushes registry modifications to disk at regular intervals of time. In addition to this regular flush operation,  registry changes are also flushed to disk at system shutdown. Allowing the 'lazy flush' to flush registry changes is the most efficient way to manage registry writes to the registry store on  disk.

The 
<b>RegFlushKey</b> function returns only when all the data for the hive that contains the specified key has been written to the registry store on disk.

The 
<b>RegFlushKey</b> function writes out the data for other keys in the hive that have been modified since the last lazy flush or system start.

 After <b>RegFlushKey</b> returns, use <a href="/windows/desktop/api/winreg/nf-winreg-regclosekey">RegCloseKey</a> to close the handle to the registry key.

## -see-also

<a href="/windows/desktop/api/winreg/nf-winreg-regclosekey">RegCloseKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regdeletekeya">RegDeleteKey</a>



<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>



<a href="/windows/desktop/SysInfo/registry">Registry Overview</a>