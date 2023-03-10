---
UID: NF:winbase.GetActiveProcessorGroupCount
title: GetActiveProcessorGroupCount function (winbase.h)
description: Returns the number of active processor groups in the system.
helpviewer_keywords: ["GetActiveProcessorGroupCount","GetActiveProcessorGroupCount function","base.getactiveprocessorgroupcount","winbase/GetActiveProcessorGroupCount"]
old-location: base\getactiveprocessorgroupcount.htm
tech.root: backup
ms.assetid: 566c6abe-9269-4e0e-9c98-e4607c808452
ms.date: 12/05/2018
ms.keywords: GetActiveProcessorGroupCount, GetActiveProcessorGroupCount function, base.getactiveprocessorgroupcount, winbase/GetActiveProcessorGroupCount
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
 - GetActiveProcessorGroupCount
 - winbase/GetActiveProcessorGroupCount
dev_langs:
 - c++
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
---

# GetActiveProcessorGroupCount function


## -description

Returns the number of active processor groups in the system.



## -returns

If the function succeeds, the return value is the number of active processor groups in the system.

If the function fails, the return value is zero.

## -remarks

To compile an application that uses this function, set _WIN32_WINNT &gt;= 0x0601. For more information, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.
