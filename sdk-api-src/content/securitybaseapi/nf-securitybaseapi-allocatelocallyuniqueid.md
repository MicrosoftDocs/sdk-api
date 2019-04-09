---
UID: NF:securitybaseapi.AllocateLocallyUniqueId
title: AllocateLocallyUniqueId function (securitybaseapi.h)
author: windows-sdk-content
description: Allocates a locally unique identifier (LUID).
old-location: security\allocatelocallyuniqueid.htm
tech.root: SecAuthZ
ms.assetid: 5d730034-802b-4d37-bd28-68992779b93e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AllocateLocallyUniqueId, AllocateLocallyUniqueId function [Security], _win32_allocatelocallyuniqueid, security.allocatelocallyuniqueid, securitybaseapi/AllocateLocallyUniqueId
ms.topic: function
req.header: securitybaseapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - AllocateLocallyUniqueId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AllocateLocallyUniqueId function


## -description


The <b>AllocateLocallyUniqueId</b> function allocates a locally unique identifier (<a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">LUID</a>).


## -parameters




### -param Luid [out]

A pointer to a <a href="https://msdn.microsoft.com/a812a46b-f23f-45b1-a6c6-48f931b78750">LUID</a> structure that receives the allocated LUID.


## -returns



If the function succeeds, the return value is nonzero. 

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The allocated <a href="https://msdn.microsoft.com/a812a46b-f23f-45b1-a6c6-48f931b78750">LUID</a> is unique to the local system only, and uniqueness is guaranteed only until the system is next restarted.

The allocated <a href="https://msdn.microsoft.com/a812a46b-f23f-45b1-a6c6-48f931b78750">LUID</a> is guaranteed  to be nonzero if this function succeeds.




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/334b8ba8-101d-43a1-a8bf-1c7e0448c272">LookupPrivilegeValue</a>
 

 

