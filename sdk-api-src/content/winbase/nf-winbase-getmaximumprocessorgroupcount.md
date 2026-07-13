---
UID: NF:winbase.GetMaximumProcessorGroupCount
title: GetMaximumProcessorGroupCount function (winbase.h)
description: Returns the maximum number of processor groups that the system can have.
helpviewer_keywords: ["GetMaximumProcessorGroupCount","GetMaximumProcessorGroupCount function","base.getmaximumprocessorgroupcount","winbase/GetMaximumProcessorGroupCount"]
old-location: base\getmaximumprocessorgroupcount.htm
tech.root: backup
ms.assetid: 7762ec89-5892-4af3-9032-bf084aef9075
ms.date: 12/05/2018
ms.keywords: GetMaximumProcessorGroupCount, GetMaximumProcessorGroupCount function, base.getmaximumprocessorgroupcount, winbase/GetMaximumProcessorGroupCount
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetMaximumProcessorGroupCount
 - winbase/GetMaximumProcessorGroupCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
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
---

# GetMaximumProcessorGroupCount function


## -description

Returns the maximum number of processor groups that the system can have.



## -returns

If the function succeeds, the return value is the maximum number of processor groups that the system can have.

If the function fails, the return value is zero.

## -remarks

To compile an application that uses this function, set _WIN32_WINNT &gt;= 0x0601. For more information, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.
