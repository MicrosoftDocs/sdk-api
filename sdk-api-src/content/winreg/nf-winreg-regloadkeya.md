---
UID: NF:winreg.RegLoadKeyA
title: RegLoadKeyA function (winreg.h)
description: Creates a subkey under HKEY_USERS or HKEY_LOCAL_MACHINE and loads the data from the specified registry hive into that subkey. (ANSI)
helpviewer_keywords: ["RegLoadKeyA", "winreg/RegLoadKeyA"]
old-location: base\regloadkey.htm
tech.root: winprog
ms.assetid: 536395aa-03ba-430d-a66d-fcabdc9dfe22
ms.date: 12/05/2018
ms.keywords: RegLoadKey, RegLoadKey function, RegLoadKeyA, RegLoadKeyW, _win32_regloadkey, base.regloadkey, winreg/RegLoadKey, winreg/RegLoadKeyA, winreg/RegLoadKeyW
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegLoadKeyW (Unicode) and RegLoadKeyA (ANSI)
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
 - RegLoadKeyA
 - winreg/RegLoadKeyA
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
 - RegLoadKey
 - RegLoadKeyA
 - RegLoadKeyW
---

# RegLoadKeyA function


## -description

Creates a subkey under <b>HKEY_USERS</b> or <b>HKEY_LOCAL_MACHINE</b> and loads the data from the specified registry hive into that subkey.

 Applications that back up or restore system state including system files and registry hives should use the <a href="/windows/win32/vss/volume-shadow-copy-service-overview">Volume Shadow Copy Service</a> instead of the registry functions.

## -parameters

### -param hKey [in]

A handle to the key where the subkey will be created. This can be a handle returned by a call to 
<a href="/windows/desktop/api/winreg/nf-winreg-regconnectregistrya">RegConnectRegistry</a>, or one of the following predefined handles: 




<b>HKEY_LOCAL_MACHINE</b>
<b>HKEY_USERS</b>
This function always loads information at the top of the registry hierarchy. The <b>HKEY_CLASSES_ROOT</b> and <b>HKEY_CURRENT_USER</b> handle values cannot be specified for this parameter, because they represent subsets of the <b>HKEY_LOCAL_MACHINE</b> and <b>HKEY_USERS</b> handle values, respectively.

### -param lpSubKey [in, optional]

The name of the key to be created under <i>hKey</i>. This subkey is where the registration information from the file will be loaded. 




Key names are not case sensitive.

For more information, see 
<a href="/windows/desktop/SysInfo/registry-element-size-limits">Registry Element Size Limits</a>.

### -param lpFile [in]

The name of the  file containing the registry data. This file must be a local file that was created with the 
<a href="/windows/desktop/api/winreg/nf-winreg-regsavekeya">RegSaveKey</a> function. If this file does not exist, a file is created with the specified name.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.

## -remarks

There are two  registry hive file formats. Registry hives created on current operating systems typically cannot be loaded by earlier ones.

If <i>hKey</i> is a handle returned by 
<a href="/windows/desktop/api/winreg/nf-winreg-regconnectregistrya">RegConnectRegistry</a>, then the path specified in <i>lpFile</i> is relative to the remote computer.

The calling process must have the SE_RESTORE_NAME and SE_BACKUP_NAME privileges on the computer in which the registry resides. For more information, see 
<a href="/windows/desktop/SecBP/running-with-special-privileges">Running with Special Privileges</a>. To load a hive without requiring these special privileges, use the <a href="/windows/desktop/api/winreg/nf-winreg-regloadappkeya">RegLoadAppKey</a> function.





> [!NOTE]
> The winreg.h header defines RegLoadKey as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winreg/nf-winreg-regconnectregistrya">RegConnectRegistry</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regdeletekeya">RegDeleteKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regloadappkeya">RegLoadAppKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regreplacekeya">RegReplaceKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regrestorekeya">RegRestoreKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regsavekeya">RegSaveKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regunloadkeya">RegUnLoadKey</a>



<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>



<a href="/windows/desktop/SysInfo/registry-hives">Registry Hive</a>
