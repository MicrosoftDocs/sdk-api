---
UID: NF:winddi.EngGetCurrentProcessId
title: EngGetCurrentProcessId function (winddi.h)
description: The EngGetCurrentProcessId function identifies an application's current process.
helpviewer_keywords: ["EngGetCurrentProcessId","EngGetCurrentProcessId function [Display Devices]","display.enggetcurrentprocessid","gdifncs_073e5c03-16d4-4257-bf0a-7ea183beea9d.xml","winddi/EngGetCurrentProcessId"]
old-location: display\enggetcurrentprocessid.htm
tech.root: display
ms.assetid: 63ed7f38-6874-4d33-80e4-fdd00175e039
ms.date: 12/05/2018
ms.keywords: EngGetCurrentProcessId, EngGetCurrentProcessId function [Display Devices], display.enggetcurrentprocessid, gdifncs_073e5c03-16d4-4257-bf0a-7ea183beea9d.xml, winddi/EngGetCurrentProcessId
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: This function is available in Windows XP and later.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: Any level
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EngGetCurrentProcessId
 - winddi/EngGetCurrentProcessId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngGetCurrentProcessId
---

# EngGetCurrentProcessId function


## -description

The <b>EngGetCurrentProcessId</b> function identifies an application's current process.



## -returns

<b>EngGetCurrentProcessId</b> returns the 4-byte identifier of the application's process.

## -remarks

Callers of <b>EngGetCurrentProcessId</b> should treat the returned ID as a read-only value.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-enggetcurrentthreadid">EngGetCurrentThreadId</a>



<a href="/windows/desktop/api/winddi/nf-winddi-enggetprocesshandle">EngGetProcessHandle</a>
