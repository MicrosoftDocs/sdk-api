---
UID: NF:jobapi2.FreeMemoryJobObject
title: FreeMemoryJobObject function (jobapi2.h)
description: Frees memory that a function related to job objects allocated. Functions related to job objects that allocate memory include QueryIoRateControlInformationJobObject.
helpviewer_keywords: ["FreeMemoryJobObject","FreeMemoryJobObject function","base.freememoryjobobject","jobapi2/FreeMemoryJobObject"]
old-location: base\freememoryjobobject.htm
tech.root: backup
ms.assetid: 8EA45FC6-A8CC-4786-8CF2-4FC868B974F2
ms.date: 12/05/2018
ms.keywords: FreeMemoryJobObject, FreeMemoryJobObject function, base.freememoryjobobject, jobapi2/FreeMemoryJobObject
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FreeMemoryJobObject
 - jobapi2/FreeMemoryJobObject
dev_langs:
 - c++
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
---

# FreeMemoryJobObject function


## -description

Frees memory that a function related to job objects allocated. Functions related to job objects that allocate memory include <a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryioratecontrolinformationjobobject">QueryIoRateControlInformationJobObject</a>.

## -parameters

### -param Buffer [in]

A pointer to the buffer of allocated memory that you want to free.

## -see-also

<a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryioratecontrolinformationjobobject">QueryIoRateControlInformationJobObject</a>