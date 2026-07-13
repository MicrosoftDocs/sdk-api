---
UID: NF:winddi.EngIsSemaphoreOwned
title: EngIsSemaphoreOwned function (winddi.h)
description: The EngIsSemaphoreOwned function determines whether any thread holds the specified semaphore.
helpviewer_keywords: ["EngIsSemaphoreOwned","EngIsSemaphoreOwned function [Display Devices]","display.engissemaphoreowned","gdifncs_9bf4c866-a563-4bc5-99d6-0189f10f0742.xml","winddi/EngIsSemaphoreOwned"]
old-location: display\engissemaphoreowned.htm
tech.root: display
ms.assetid: a04f6f46-f075-40d1-8b56-d37a80fb3571
ms.date: 12/05/2018
ms.keywords: EngIsSemaphoreOwned, EngIsSemaphoreOwned function [Display Devices], display.engissemaphoreowned, gdifncs_9bf4c866-a563-4bc5-99d6-0189f10f0742.xml, winddi/EngIsSemaphoreOwned
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
 - EngIsSemaphoreOwned
 - winddi/EngIsSemaphoreOwned
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
 - EngIsSemaphoreOwned
---

# EngIsSemaphoreOwned function


## -description

The <b>EngIsSemaphoreOwned</b> function determines whether any thread holds the specified semaphore.

## -parameters

### -param hsem [in]

Handle to the semaphore.

## -returns

<b>EngIsSemaphoreOwned</b> returns <b>TRUE</b> if any thread holds the specified semaphore, and <b>FALSE</b> if no thread holds it.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engacquiresemaphore">EngAcquireSemaphore</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engcreatesemaphore">EngCreateSemaphore</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engissemaphoreownedbycurrentthread">EngIsSemaphoreOwnedByCurrentThread</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engreleasesemaphore">EngReleaseSemaphore</a>