---
UID: NF:winddi.EngGetLastError
title: EngGetLastError function (winddi.h)
description: The EngGetLastError function returns the last error code logged by GDI for the calling thread.
helpviewer_keywords: ["EngGetLastError","EngGetLastError function [Display Devices]","display.enggetlasterror","gdifncs_19c92fa6-2204-40e7-adc5-22a85b9ba0d5.xml","winddi/EngGetLastError"]
old-location: display\enggetlasterror.htm
tech.root: display
ms.assetid: 47138077-125e-4da9-b0de-e437a9b1733d
ms.date: 12/05/2018
ms.keywords: EngGetLastError, EngGetLastError function [Display Devices], display.enggetlasterror, gdifncs_19c92fa6-2204-40e7-adc5-22a85b9ba0d5.xml, winddi/EngGetLastError
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EngGetLastError
 - winddi/EngGetLastError
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-base-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngGetLastError
---

# EngGetLastError function


## -description

The <b>EngGetLastError</b> function returns the last error code logged by GDI for the calling thread.



## -returns

The return value is the last error code set by <b>EngSetLastError</b>.

## -remarks

<b>EngGetLastError</b> facilitates communication of GDI and/or driver error conditions to an application.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engsetlasterror">EngSetLastError</a>
