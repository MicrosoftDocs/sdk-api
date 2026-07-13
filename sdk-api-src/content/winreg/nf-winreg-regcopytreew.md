---
UID: NF:winreg.RegCopyTreeW
title: RegCopyTreeW function (winreg.h)
description: Copies the specified registry key, along with its values and subkeys, to the specified destination key. (Unicode)
helpviewer_keywords: ["RegCopyTree", "RegCopyTree function", "RegCopyTreeW", "base.regcopytree", "winreg/RegCopyTree", "winreg/RegCopyTreeW"]
old-location: base\regcopytree.htm
tech.root: winprog
ms.assetid: d16f2b47-e537-42b0-90b3-9f9a00e61e76
ms.date: 12/05/2018
ms.keywords: RegCopyTree, RegCopyTree function, RegCopyTreeA, RegCopyTreeW, base.regcopytree, winreg/RegCopyTree, winreg/RegCopyTreeA, winreg/RegCopyTreeW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegCopyTreeW
 - winreg/RegCopyTreeW
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
---

# RegCopyTreeW function


## -description

Copies the specified registry key, along with its values and subkeys, to the specified destination key.

## -parameters

### -param hKeySrc [in]

A handle to an open registry key. The key must have been opened with the KEY_READ access right. For more information, see 
<a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>. 




This handle is returned by the 
<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a> or 
<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a> function, or it can be one of the <a href="/windows/desktop/SysInfo/predefined-keys">predefined keys</a>.

### -param lpSubKey [in, optional]

The name of the key. This key must be a subkey of the key identified by the <i>hKeySrc</i> parameter. This parameter can also be <b>NULL</b>.

### -param hKeyDest [in]

A handle to the destination key. The calling process  must have KEY_CREATE_SUB_KEY access to the key.  




This handle is returned by the 
<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a> or 
<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a> function, or it can be one of the <a href="/windows/desktop/SysInfo/predefined-keys">predefined keys</a>.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.

## -remarks

This function also copies the security descriptor for the key.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.





> [!NOTE]
> The winreg.h header defines RegCopyTree as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>
