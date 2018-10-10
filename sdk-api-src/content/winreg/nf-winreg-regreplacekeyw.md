---
UID: NF:winreg.RegReplaceKeyW
title: RegReplaceKeyW function
author: windows-sdk-content
description: Replaces the file backing a registry key and all its subkeys with another file, so that when the system is next started, the key and subkeys will have the values stored in the new file.
old-location: base\regreplacekey.htm
tech.root: SysInfo
ms.assetid: f968fa71-edc8-4f49-b9fa-1e89224df33b
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: RegReplaceKey, RegReplaceKey function, RegReplaceKeyA, RegReplaceKeyW, _win32_regreplacekey, base.regreplacekey, winreg/RegReplaceKey, winreg/RegReplaceKeyA, winreg/RegReplaceKeyW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegReplaceKeyW (Unicode) and RegReplaceKeyA (ANSI)
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
 - API-MS-Win-Core-Registry-l2-1-0.dll
 - advapi32legacy.dll
 - API-MS-Win-Core-Registry-l2-2-0.dll
api_name:
 - RegReplaceKey
 - RegReplaceKeyA
 - RegReplaceKeyW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RegReplaceKeyW function


## -description


Replaces the file backing a registry key and all its subkeys with another file, so that when the system is next started, the key and subkeys will have the values stored in the new file.

 Applications that back up or restore system state including system files and registry hives should use the <a href="http://go.microsoft.com/fwlink/p/?linkid=177790">Volume Shadow Copy Service</a> instead of the registry functions.


## -parameters




### -param hKey [in]

A handle to an open registry key. This handle is returned by the 
<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a> or 
<a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a> function, or it can be one of the following 
<a href="https://msdn.microsoft.com/db747656-b414-4594-ad39-6b476799060c">predefined keys</a>: 




<b>HKEY_CLASSES_ROOT</b>
<b>HKEY_CURRENT_CONFIG</b>
<b>HKEY_CURRENT_USER</b>
<b>HKEY_LOCAL_MACHINE</b>
<b>HKEY_USERS</b>

### -param lpSubKey [in, optional]

The name of the registry key whose subkeys and values are to be replaced. If the key exists, it must be a subkey of the key identified by the <i>hKey</i> parameter. If the subkey does not exist, it is created. This parameter can be <b>NULL</b>. 




If the specified subkey is not the root of a hive, 
<b>RegReplaceKey</b> traverses up the hive tree structure until it encounters a hive root, then it replaces the contents of that hive with the contents of the data file specified by <i>lpNewFile</i>.

For more information, see 
<a href="https://msdn.microsoft.com/a6d3a884-f181-46a5-b655-226c68792e08">Registry Element Size Limits</a>.


### -param lpNewFile [in]

The name of the file with the registry information. This file is typically created by using the 
<a href="https://msdn.microsoft.com/da80f40d-0099-4748-94ca-5d3b001e633e">RegSaveKey</a> function.


### -param lpOldFile [in]

The name of the file that receives a backup copy of the registry information being replaced.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.




## -remarks



There are two different registry hive file formats. Registry hives created on current operating systems typically cannot be loaded by earlier ones.

The file specified by the <i>lpNewFile</i> parameter remains open until the system is restarted.

If <i>hKey</i> is a handle returned by 
<a href="https://msdn.microsoft.com/d7fb41cc-4855-4ad7-879c-b1ac85ac5803">RegConnectRegistry</a>, then the paths specified in <i>lpNewFile</i> and <i>lpOldFile</i> are relative to the remote computer.

The calling process must have the SE_RESTORE_NAME and SE_BACKUP_NAME privileges on the computer in which the registry resides. For more information, see 
<a href="https://msdn.microsoft.com/b25db548-d5ab-4276-9b50-36d030909384">Running with Special Privileges</a>.




## -see-also




<a href="https://msdn.microsoft.com/d7fb41cc-4855-4ad7-879c-b1ac85ac5803">RegConnectRegistry</a>



<a href="https://msdn.microsoft.com/a2310ca0-1b9f-48d1-a3b5-ea3a528bfaba">RegDeleteKey</a>



<a href="https://msdn.microsoft.com/536395aa-03ba-430d-a66d-fcabdc9dfe22">RegLoadKey</a>



<a href="https://msdn.microsoft.com/6267383d-427a-4ae8-b9cc-9c1861d3b7bb">RegRestoreKey</a>



<a href="https://msdn.microsoft.com/da80f40d-0099-4748-94ca-5d3b001e633e">RegSaveKey</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>



<a href="https://msdn.microsoft.com/ffb06903-593e-47ce-adb2-baed5d379110">Registry Overview</a>
 

 

