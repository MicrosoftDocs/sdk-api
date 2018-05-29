---
UID: NF:winreg.RegDisablePredefinedCacheEx
title: RegDisablePredefinedCacheEx function
author: windows-sdk-content
description: Disables handle caching for all predefined registry handles for the current process.
old-location: base\regdisablepredefinedcacheex.htm
old-project: SysInfo
ms.assetid: a56cf7d9-0ac4-4719-af41-3c0cdcef6faf
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: RegDisablePredefinedCacheEx, RegDisablePredefinedCacheEx function, base.regdisablepredefinedcacheex, winreg/RegDisablePredefinedCacheEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PERF_OBJECT_TYPE, *PPERF_OBJECT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Advapi32.dll
-	API-MS-Win-Core-Localregistry-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-Registry-l1-1-0.dll
-	API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
-	API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
-	MinKernelBase.dll
-	api-ms-win-core-registry-l1-1-1.dll
api_name:
-	RegDisablePredefinedCacheEx
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RegDisablePredefinedCacheEx function


## -description


Disables handle caching for all predefined registry handles for the current process.


## -parameters






## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



This function does not work on a remote computer.

Services that change impersonation should call this function before using any of the predefined handles.

For example, any access of <b>HKEY_CURRENT_USER</b> after this function is called results in open and close operations being performed on <b>HKEY_USERS</b>\<b>SID_of_current_user</b>, or on <b>HKEY_USERS\.DEFAULT</b> if the current user's hive is not loaded. For more information on SIDs, see 
<a href="security.security_identifiers_sids_">Security Identifiers</a>.




## -see-also




<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a>



<a href="https://msdn.microsoft.com/db747656-b414-4594-ad39-6b476799060c">Predefined Keys</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>
 

 

