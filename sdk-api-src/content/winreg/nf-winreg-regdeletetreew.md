---
UID: NF:winreg.RegDeleteTreeW
title: RegDeleteTreeW function (winreg.h)
description: Deletes the subkeys and values of the specified key recursively. (Unicode)
helpviewer_keywords: ["RegDeleteTree", "RegDeleteTree function", "RegDeleteTreeW", "base.regdeletetree", "winreg/RegDeleteTree", "winreg/RegDeleteTreeW"]
old-location: base\regdeletetree.htm
tech.root: winprog
ms.assetid: 984813a9-e191-498f-8288-b8a4c567112b
ms.date: 12/05/2018
ms.keywords: RegDeleteTree, RegDeleteTree function, RegDeleteTreeA, RegDeleteTreeW, base.regdeletetree, winreg/RegDeleteTree, winreg/RegDeleteTreeA, winreg/RegDeleteTreeW
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegDeleteTreeW (Unicode) and RegDeleteTreeA (ANSI)
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
 - RegDeleteTreeW
 - winreg/RegDeleteTreeW
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
 - RegDeleteTree
 - RegDeleteTreeA
 - RegDeleteTreeW
---

# RegDeleteTreeW function


## -description

Deletes the subkeys and values of the specified key recursively.

## -parameters

### -param hKey [in]

A handle to an open registry key. The key must have been opened with the following access rights: DELETE, KEY_ENUMERATE_SUB_KEYS, and KEY_QUERY_VALUE. For more information, see 
<a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>.

This handle is returned by the
<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a>,
<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeytransacteda">RegCreateKeyTransacted</a>,
<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a>, or
<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeytransacteda">RegOpenKeyTransacted</a> function,
or it can be one of the following 
<a href="/windows/desktop/SysInfo/predefined-keys">Predefined Keys</a>:<dl>
<dd><b>HKEY_CLASSES_ROOT</b></dd>
<dd><b>HKEY_CURRENT_CONFIG</b></dd>
<dd><b>HKEY_CURRENT_USER</b></dd>
<dd><b>HKEY_LOCAL_MACHINE</b></dd>
<dd><b>HKEY_USERS</b></dd>
</dl>

### -param lpSubKey [in, optional]

The name of the key. This key must be a subkey of the key identified by the <i>hKey</i> parameter. If this parameter is <b>NULL</b>, the subkeys and values of <i>hKey</i> are deleted.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.

## -remarks

If the key has values, it must be opened with KEY_SET_VALUE or this function will fail with ERROR_ACCESS_DENIED.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.



> [!NOTE] 
> On legacy versions of Windows, this API is also exposed by kernel32.dll.

> [!NOTE]
> The winreg.h header defines RegDeleteTree as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winreg/nf-winreg-regdeletekeya">RegDeleteKey</a>

<a href="/windows/desktop/api/winreg/nf-winreg-regdeletekeyexa">RegDeleteKeyEx</a>

<a href="/windows/desktop/api/winreg/nf-winreg-regdeletekeytransacteda">RegDeleteKeyTransacted</a>

<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>
