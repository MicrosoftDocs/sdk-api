---
UID: NF:winreg.RegLoadKeyA
title: RegLoadKeyA function
author: windows-sdk-content
description: Creates a subkey under HKEY_USERS or HKEY_LOCAL_MACHINE and loads the data from the specified registry hive into that subkey.
old-location: base\regloadkey.htm
old-project: sysinfo
ms.assetid: 536395aa-03ba-430d-a66d-fcabdc9dfe22
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: RegLoadKey, RegLoadKey function, RegLoadKeyA, RegLoadKeyW, _win32_regloadkey, base.regloadkey, winreg/RegLoadKey, winreg/RegLoadKeyA, winreg/RegLoadKeyW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: PERF_OBJECT_TYPE, *PPERF_OBJECT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RegLoadKeyA function


## -description


Creates a subkey under <b>HKEY_USERS</b> or <b>HKEY_LOCAL_MACHINE</b> and loads the data from the specified registry hive into that subkey.

 Applications that back up or restore system state including system files and registry hives should use the <a href="http://go.microsoft.com/fwlink/p/?linkid=177790">Volume Shadow Copy Service</a> instead of the registry functions.


## -parameters




### -param hKey [in]

A handle to the key where the subkey will be created. This can be a handle returned by a call to 
<a href="https://msdn.microsoft.com/d7fb41cc-4855-4ad7-879c-b1ac85ac5803">RegConnectRegistry</a>, or one of the following predefined handles: 




<b>HKEY_LOCAL_MACHINE</b>
<b>HKEY_USERS</b>
This function always loads information at the top of the registry hierarchy. The <b>HKEY_CLASSES_ROOT</b> and <b>HKEY_CURRENT_USER</b> handle values cannot be specified for this parameter, because they represent subsets of the <b>HKEY_LOCAL_MACHINE</b> and <b>HKEY_USERS</b> handle values, respectively.


### -param lpSubKey [in, optional]

The name of the key to be created under <i>hKey</i>. This subkey is where the registration information from the file will be loaded. 




Key names are not case sensitive.

For more information, see 
<a href="https://msdn.microsoft.com/a6d3a884-f181-46a5-b655-226c68792e08">Registry Element Size Limits</a>.


### -param lpFile [in]

The name of the  file containing the registry data. This file must be a local file that was created with the 
<a href="https://msdn.microsoft.com/da80f40d-0099-4748-94ca-5d3b001e633e">RegSaveKey</a> function. If this file does not exist, a file is created with the specified name.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.




## -remarks



There are two  registry hive file formats. Registry hives created on current operating systems typically cannot be loaded by earlier ones.

If <i>hKey</i> is a handle returned by 
<a href="https://msdn.microsoft.com/d7fb41cc-4855-4ad7-879c-b1ac85ac5803">RegConnectRegistry</a>, then the path specified in <i>lpFile</i> is relative to the remote computer.

The calling process must have the SE_RESTORE_NAME and SE_BACKUP_NAME privileges on the computer in which the registry resides. For more information, see 
<a href="https://msdn.microsoft.com/b25db548-d5ab-4276-9b50-36d030909384">Running with Special Privileges</a>. To load a hive without requiring these special privileges, use the <a href="https://msdn.microsoft.com/88eb79c1-9ea0-436e-ad2e-9ce05b8dcb2c">RegLoadAppKey</a> function.




## -see-also




<a href="https://msdn.microsoft.com/d7fb41cc-4855-4ad7-879c-b1ac85ac5803">RegConnectRegistry</a>



<a href="https://msdn.microsoft.com/a2310ca0-1b9f-48d1-a3b5-ea3a528bfaba">RegDeleteKey</a>



<a href="https://msdn.microsoft.com/88eb79c1-9ea0-436e-ad2e-9ce05b8dcb2c">RegLoadAppKey</a>



<a href="https://msdn.microsoft.com/f968fa71-edc8-4f49-b9fa-1e89224df33b">RegReplaceKey</a>



<a href="https://msdn.microsoft.com/6267383d-427a-4ae8-b9cc-9c1861d3b7bb">RegRestoreKey</a>



<a href="https://msdn.microsoft.com/da80f40d-0099-4748-94ca-5d3b001e633e">RegSaveKey</a>



<a href="https://msdn.microsoft.com/73b4b6a9-4acb-4247-bd7f-82024ba3e14a">RegUnLoadKey</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>



<a href="https://msdn.microsoft.com/fe517d88-7b03-4dc3-b3db-6a92665bca8e">Registry Hive</a>
 

 

