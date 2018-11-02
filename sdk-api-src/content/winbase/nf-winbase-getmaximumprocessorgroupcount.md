---
UID: NF:winbase.GetMaximumProcessorGroupCount
title: GetMaximumProcessorGroupCount function
author: windows-sdk-content
description: Returns the maximum number of processor groups that the system can have.
old-location: base\getmaximumprocessorgroupcount.htm
tech.root: procthread
ms.assetid: 7762ec89-5892-4af3-9032-bf084aef9075
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetMaximumProcessorGroupCount, GetMaximumProcessorGroupCount function, base.getmaximumprocessorgroupcount, winbase/GetMaximumProcessorGroupCount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - GetMaximumProcessorGroupCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetMaximumProcessorGroupCount function


## -description


Returns the maximum number of processor groups that the system can have. 


## -parameters






## -returns



If the function succeeds, the return value is the maximum number of processor groups that the system can have.

If the function fails, the return value is zero.




## -remarks



To compile an application that uses this function, set _WIN32_WINNT &gt;= 0x0601. For more information, see <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.



