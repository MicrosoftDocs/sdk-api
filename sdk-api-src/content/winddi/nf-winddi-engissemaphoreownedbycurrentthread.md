---
UID: NF:winddi.EngIsSemaphoreOwnedByCurrentThread
title: EngIsSemaphoreOwnedByCurrentThread function (winddi.h)
description: The EngIsSemaphoreOwnedByCurrentThread function determines whether the currently executing thread holds the specified semaphore.
helpviewer_keywords: ["EngIsSemaphoreOwnedByCurrentThread","EngIsSemaphoreOwnedByCurrentThread function [Display Devices]","display.engissemaphoreownedbycurrentthread","gdifncs_6c3dcc33-1798-4dc5-a64f-a9bb85f5cf81.xml","winddi/EngIsSemaphoreOwnedByCurrentThread"]
old-location: display\engissemaphoreownedbycurrentthread.htm
tech.root: display
ms.assetid: ce5d8ceb-0137-4ca9-b718-2e3de650249d
ms.date: 12/05/2018
ms.keywords: EngIsSemaphoreOwnedByCurrentThread, EngIsSemaphoreOwnedByCurrentThread function [Display Devices], display.engissemaphoreownedbycurrentthread, gdifncs_6c3dcc33-1798-4dc5-a64f-a9bb85f5cf81.xml, winddi/EngIsSemaphoreOwnedByCurrentThread
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
 - EngIsSemaphoreOwnedByCurrentThread
 - winddi/EngIsSemaphoreOwnedByCurrentThread
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
 - EngIsSemaphoreOwnedByCurrentThread
---

# EngIsSemaphoreOwnedByCurrentThread function


## -description

The <b>EngIsSemaphoreOwnedByCurrentThread</b> function determines whether the currently executing thread holds the specified semaphore.

## -parameters

### -param hsem [in]

Handle to the semaphore.

## -returns

<b>EngIsSemaphoreOwnedByCurrentThread</b> returns <b>TRUE</b> if the currently executing thread holds the specified semaphore, and <b>FALSE</b> if it does not.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engacquiresemaphore">EngAcquireSemaphore</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engcreatesemaphore">EngCreateSemaphore</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engissemaphoreowned">EngIsSemaphoreOwned</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engreleasesemaphore">EngReleaseSemaphore</a>