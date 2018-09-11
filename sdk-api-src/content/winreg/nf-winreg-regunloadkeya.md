---
UID: NF:winreg.RegUnLoadKeyA
title: RegUnLoadKeyA function
author: windows-sdk-content
description: Unloads the specified registry key and its subkeys from the registry.
old-location: base\regunloadkey.htm
tech.root: SysInfo
ms.assetid: 73b4b6a9-4acb-4247-bd7f-82024ba3e14a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: RegUnLoadKey, RegUnLoadKey function, RegUnLoadKeyA, RegUnLoadKeyW, _win32_regunloadkey, base.regunloadkey, winreg/RegUnLoadKey, winreg/RegUnLoadKeyA, winreg/RegUnLoadKeyW
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
req.unicode-ansi: RegUnLoadKeyW (Unicode) and RegUnLoadKeyA (ANSI)
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
 - API-MS-Win-Core-Localregistry-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Registry-l1-1-0.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - MinKernelBase.dll
 - api-ms-win-core-registry-l1-1-1.dll
api_name:
 - RegUnLoadKey
 - RegUnLoadKeyA
 - RegUnLoadKeyW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RegUnLoadKeyA function


## -description


Unloads the specified registry key and its subkeys from the registry.

 Applications that back up or restore system state including system files and registry hives should use the <a href="http://go.microsoft.com/fwlink/p/?linkid=177790">Volume Shadow Copy Service</a> instead of the registry functions.


## -parameters




### -param hKey [in]

A handle to the registry key to be unloaded. This parameter can be a handle returned by a call to 
<a href="https://msdn.microsoft.com/d7fb41cc-4855-4ad7-879c-b1ac85ac5803">RegConnectRegistry</a> function or one of the following predefined handles: 




<b>HKEY_LOCAL_MACHINE</b>
<b>HKEY_USERS</b>

### -param lpSubKey [in, optional]

The name of the subkey to be unloaded. The key referred to by the <i>lpSubKey</i> parameter must have been created by using the 
<a href="https://msdn.microsoft.com/536395aa-03ba-430d-a66d-fcabdc9dfe22">RegLoadKey</a> function. 




Key names are not case sensitive.

For more information, see 
<a href="https://msdn.microsoft.com/a6d3a884-f181-46a5-b655-226c68792e08">Registry Element Size Limits</a>.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.




## -remarks



This function removes a hive from the registry but does not modify the file containing the registry information. A hive is a discrete body of keys, subkeys, and values that is rooted at the top of the registry hierarchy.

The calling process must have the SE_RESTORE_NAME and SE_BACKUP_NAME privileges on the computer in which the registry resides. For more information, see 
<a href="https://msdn.microsoft.com/b25db548-d5ab-4276-9b50-36d030909384">Running with Special Privileges</a>.




## -see-also




<a href="https://msdn.microsoft.com/d7fb41cc-4855-4ad7-879c-b1ac85ac5803">RegConnectRegistry</a>



<a href="https://msdn.microsoft.com/a2310ca0-1b9f-48d1-a3b5-ea3a528bfaba">RegDeleteKey</a>



<a href="https://msdn.microsoft.com/536395aa-03ba-430d-a66d-fcabdc9dfe22">RegLoadKey</a>



<a href="https://msdn.microsoft.com/6267383d-427a-4ae8-b9cc-9c1861d3b7bb">RegRestoreKey</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>



<a href="https://msdn.microsoft.com/ffb06903-593e-47ce-adb2-baed5d379110">Registry Overview</a>
 

 

