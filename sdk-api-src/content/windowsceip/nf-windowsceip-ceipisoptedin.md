---
UID: NF:windowsceip.CeipIsOptedIn
title: CeipIsOptedIn function (windowsceip.h)
description: Checks whether the user has opted in for SQM data collection as part of the Customer Experience Improvement Program (CEIP).
helpviewer_keywords: ["CeipIsOptedIn","CeipIsOptedIn function","base.ceipisoptedin","windowsceip/ CeipIsOptedIn"]
old-location: base\ceipisoptedin.htm
tech.root: winprog
ms.assetid: 4CDB5B09-B172-4E99-AB46-A08E32346266
ms.date: 12/05/2018
ms.keywords: CeipIsOptedIn, CeipIsOptedIn function, base.ceipisoptedin, windowsceip/ CeipIsOptedIn
req.header: windowsceip.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - CeipIsOptedIn
 - windowsceip/CeipIsOptedIn
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Windowsceip-L1-1-0.dll
 - KernelBase.dll
api_name:
 - CeipIsOptedIn
---

# CeipIsOptedIn function


## -description

Checks whether the user has opted in for SQM data collection as part of the Customer Experience Improvement Program (CEIP).



## -returns

True if SQM data collection is opted in and the machine can send data. Otherwise, false.

## -see-also

<a href="/windows/desktop/DevNotes/ceipenable">CEIPEnable</a>

<a href="/windows/compatibility">Windows and Windows Server Compatibility Cookbook</a>
