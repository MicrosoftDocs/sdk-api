---
UID: NF:winbase.GetActiveProcessorGroupCount
title: GetActiveProcessorGroupCount function
author: windows-sdk-content
description: Returns the number of active processor groups in the system.
old-location: base\getactiveprocessorgroupcount.htm
old-project: procthread
ms.assetid: 566c6abe-9269-4e0e-9c98-e4607c808452
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: GetActiveProcessorGroupCount, GetActiveProcessorGroupCount function, base.getactiveprocessorgroupcount, winbase/GetActiveProcessorGroupCount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - API-MS-Win-Core-ProcessTopology-Obsolete-L1-1-1.dll
 - Kernel32Legacy.dll
api_name:
 - GetActiveProcessorGroupCount
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetActiveProcessorGroupCount function


## -description


Returns the number of active processor groups in the system.


## -parameters






## -returns



If the function succeeds, the return value is the number of active processor groups in the system.

If the function fails, the return value is zero.




## -remarks



To compile an application that uses this function, set _WIN32_WINNT &gt;= 0x0601. For more information, see <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.



