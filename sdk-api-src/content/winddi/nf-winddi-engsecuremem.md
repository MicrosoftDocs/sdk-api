---
UID: NF:winddi.EngSecureMem
title: EngSecureMem function (winddi.h)
description: The EngSecureMem function locks down the specified address range in memory.
helpviewer_keywords: ["EngSecureMem","EngSecureMem function [Display Devices]","display.engsecuremem","gdifncs_b152193e-5e03-4223-b847-8dc99aeb0852.xml","winddi/EngSecureMem"]
old-location: display\engsecuremem.htm
tech.root: display
ms.assetid: 30c1e7bb-5300-4c0f-871d-a1c09fa83fdd
ms.date: 12/05/2018
ms.keywords: EngSecureMem, EngSecureMem function [Display Devices], display.engsecuremem, gdifncs_b152193e-5e03-4223-b847-8dc99aeb0852.xml, winddi/EngSecureMem
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
 - EngSecureMem
 - winddi/EngSecureMem
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
 - EngSecureMem
---

# EngSecureMem function


## -description

The <b>EngSecureMem</b> function locks down the specified address range in memory.

## -parameters

### -param Address [in]

Pointer to the base address of the memory to be secured.

### -param Length [in]

Specifies the size of the memory range to be secured.

## -returns

<b>EngSecureMem</b> returns a handle to the secured address range upon successful completion; otherwise, it returns <b>NULL</b>.

## -remarks

The address range locked down by <b>EngSecureMem</b> will not be deallocated until it is unlocked by <a href="/windows/desktop/api/winddi/nf-winddi-engunsecuremem">EngUnsecureMem</a>.