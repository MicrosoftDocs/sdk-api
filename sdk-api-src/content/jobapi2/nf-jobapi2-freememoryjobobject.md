---
UID: NF:jobapi2.FreeMemoryJobObject
title: FreeMemoryJobObject function
author: windows-sdk-content
description: Frees memory that a function related to job objects allocated. Functions related to job objects that allocate memory include QueryIoRateControlInformationJobObject.
old-location: base\freememoryjobobject.htm
tech.root: procthread
ms.assetid: 8EA45FC6-A8CC-4786-8CF2-4FC868B974F2
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: FreeMemoryJobObject, FreeMemoryJobObject function, base.freememoryjobobject, jobapi2/FreeMemoryJobObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: jobapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - API-MS-Win-Core-Job-L2-1-1.dll
 - Kernel32Legacy.dll
api_name:
 - FreeMemoryJobObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FreeMemoryJobObject function


## -description


Frees memory that a function related to job objects allocated. Functions related to job objects that allocate memory include <a href="https://msdn.microsoft.com/B61DA8FC-1CF7-4D97-86F5-E3C2131D41EC">QueryIoRateControlInformationJobObject</a>.  


## -parameters




### -param Buffer [in]

A pointer to the buffer of allocated memory that you want to free.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/B61DA8FC-1CF7-4D97-86F5-E3C2131D41EC">QueryIoRateControlInformationJobObject</a>
 

 

