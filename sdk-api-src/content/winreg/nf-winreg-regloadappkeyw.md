---
UID: NF:winreg.RegLoadAppKeyW
title: RegLoadAppKeyW function (winreg.h)
description: Loads the specified registry hive as an application hive. (Unicode)
helpviewer_keywords: ["RegLoadAppKey", "RegLoadAppKey function", "RegLoadAppKeyW", "base.regloadappkey", "winreg/RegLoadAppKey", "winreg/RegLoadAppKeyW"]
old-location: base\regloadappkey.htm
tech.root: winprog
ms.assetid: 88eb79c1-9ea0-436e-ad2e-9ce05b8dcb2c
ms.date: 12/05/2018
ms.keywords: RegLoadAppKey, RegLoadAppKey function, RegLoadAppKeyA, RegLoadAppKeyW, base.regloadappkey, winreg/RegLoadAppKey, winreg/RegLoadAppKeyA, winreg/RegLoadAppKeyW
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegLoadAppKeyW (Unicode) and RegLoadAppKeyA (ANSI)
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
 - RegLoadAppKeyW
 - winreg/RegLoadAppKeyW
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
 - API-MS-Win-Core-Registry-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - MinKernelBase.dll
 - api-ms-win-core-registry-l1-1-1.dll
api_name:
 - RegLoadAppKey
 - RegLoadAppKeyA
 - RegLoadAppKeyW
---

# RegLoadAppKeyW function


## -description

Loads the specified registry hive as an application hive.

## -parameters

### -param lpFile [in]

The name of the  hive file. This hive must have been created with the 
<a href="/windows/desktop/api/winreg/nf-winreg-regsavekeya">RegSaveKey</a> or <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeyexa">RegSaveKeyEx</a> function. If the  file does not exist, an empty hive file is created with the specified name.

### -param phkResult [out]

Pointer to the handle for the root key of the loaded hive.

The only way to access keys in the hive is through this handle. The registry will prevent an application from accessing keys in this hive using an absolute path to the key. As a result, it is not possible to navigate to this hive through the registry's namespace.

### -param samDesired [in]

A mask that specifies the access rights requested for the returned root key. For more information, see 
<a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>.

### -param dwOptions [in]

If this parameter is REG_PROCESS_APPKEY, the hive cannot be loaded again  while it is loaded by the caller. This prevents access to this registry hive by another caller.

### -param Reserved

This parameter is reserved.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.

## -remarks

Unlike <a href="/windows/desktop/api/winreg/nf-winreg-regloadkeya">RegLoadKey</a>, <b>RegLoadAppKey</b> does not load the hive under HKEY_LOCAL_MACHINE or HKEY_USERS. Instead, the hive is loaded under a special root that cannot be enumerated. As a result, there is no way to enumerate hives currently loaded by <b>RegLoadAppKey</b>. All operations on hives loaded by <b>RegLoadAppKey</b> have to be performed relative to the handle returned in <i>phkResult.</i>

 

If two processes are required to perform operations on the same hive, each process must call <b>RegLoadAppKey</b> to retrieve a handle. During the <b>RegLoadAppKey</b> operation, the registry will  verify if the  file has already been loaded. If it has been loaded, the registry will return a handle to the previously loaded hive rather than re-loading the hive. 


All keys inside the hive must have the same security descriptor, otherwise the function will fail. This security descriptor must grant the caller the access specified by the <i>samDesired</i> parameter or the function will fail. You cannot use the <a href="/windows/desktop/api/winreg/nf-winreg-regsetkeysecurity">RegSetKeySecurity</a> function on any key inside the hive.

In Windows 8 and later, each process can call <b>RegLoadAppKey</b> to load multiple hives. In Windows 7 and earlier, each process can load only one hive using <b>RegLoadAppKey</b> at a time.

Any hive loaded using <b>RegLoadAppKey</b> is automatically unloaded when all handles to the keys inside the hive are closed using <a href="/windows/desktop/api/winreg/nf-winreg-regclosekey">RegCloseKey</a>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.





> [!NOTE]
> The winreg.h header defines RegLoadAppKey as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winreg/nf-winreg-regsavekeya">RegSaveKey</a>



<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>



<a href="/windows/desktop/SysInfo/registry-hives">Registry Hive</a>
