---
UID: NF:winreg.RegLoadAppKeyA
title: RegLoadAppKeyA function
author: windows-sdk-content
description: Loads the specified registry hive as an application hive.
old-location: base\regloadappkey.htm
old-project: SysInfo
ms.assetid: 88eb79c1-9ea0-436e-ad2e-9ce05b8dcb2c
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: RegLoadAppKey, RegLoadAppKey function, RegLoadAppKeyA, RegLoadAppKeyW, base.regloadappkey, winreg/RegLoadAppKey, winreg/RegLoadAppKeyA, winreg/RegLoadAppKeyW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winreg.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: PERF_OBJECT_TYPE, *PPERF_OBJECT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RegLoadAppKeyA function


## -description


Loads the specified registry hive as an application hive.


## -parameters




### -param lpFile [in]

The name of the  hive file. This hive must have been created with the 
<a href="https://msdn.microsoft.com/da80f40d-0099-4748-94ca-5d3b001e633e">RegSaveKey</a> or <a href="https://msdn.microsoft.com/f93b4162-cac4-42f7-bfd4-9e23fff80a03">RegSaveKeyEx</a> function. If the  file does not exist, an empty hive file is created with the specified name.


### -param phkResult [out]

Pointer to the handle for the root key of the loaded hive.

The only way to access keys in the hive is through this handle. The registry will prevent an application from accessing keys in this hive using an absolute path to the key. As a result, it is not possible to navigate to this hive through the registry's namespace.


### -param samDesired [in]

A mask that specifies the access rights requested for the returned root key. For more information, see 
<a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>.


### -param dwOptions [in]

If this parameter is REG_PROCESS_APPKEY, the hive cannot be loaded again  while it is loaded by the caller. This prevents access to this registry hive by another caller.


### -param Reserved

This parameter is reserved.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.




## -remarks



Unlike <a href="https://msdn.microsoft.com/536395aa-03ba-430d-a66d-fcabdc9dfe22">RegLoadKey</a>, <b>RegLoadAppKey</b> does not load the hive under HKEY_LOCAL_MACHINE or HKEY_USERS. Instead, the hive is loaded under a special root that cannot be enumerated. As a result, there is no way to enumerate hives currently loaded by <b>RegLoadAppKey</b>. All operations on hives loaded by <b>RegLoadAppKey</b> have to be performed relative to the handle returned in <i>phkResult.</i>

 

If two processes are required to perform operations on the same hive, each process must call <b>RegLoadAppKey</b> to retrieve a handle. During the <b>RegLoadAppKey</b> operation, the registry will  verify if the  file has already been loaded. If it has been loaded, the registry will return a handle to the previously loaded hive rather than re-loading the hive. 


All keys inside the hive must have the same security descriptor, otherwise the function will fail. This security descriptor must grant the caller the access specified by the <i>samDesired</i> parameter or the function will fail. You cannot use the <a href="https://msdn.microsoft.com/08bf8fc1-6a08-490e-b589-730211774257">RegSetKeySecurity</a> function on any key inside the hive.

In Windows 8 and later, each process can call <b>RegLoadAppKey</b> to load multiple hives. In Windows 7 and earlier, each process can load only one hive using <b>RegLoadAppKey</b> at a time.

Any hive loaded using <b>RegLoadAppKey</b> is automatically unloaded when all handles to the keys inside the hive are closed using <a href="https://msdn.microsoft.com/10175499-abf3-4694-9594-bb97b43f3fa5">RegCloseKey</a>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/da80f40d-0099-4748-94ca-5d3b001e633e">RegSaveKey</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>



<a href="https://msdn.microsoft.com/fe517d88-7b03-4dc3-b3db-6a92665bca8e">Registry Hive</a>
 

 

