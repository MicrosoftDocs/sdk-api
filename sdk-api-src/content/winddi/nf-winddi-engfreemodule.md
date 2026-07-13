---
UID: NF:winddi.EngFreeModule
title: EngFreeModule function (winddi.h)
description: The EngFreeModule function unmaps a file from system memory.
helpviewer_keywords: ["EngFreeModule","EngFreeModule function [Display Devices]","display.engfreemodule","gdifncs_23d84e6d-60e7-43a4-af20-3234c8581190.xml","winddi/EngFreeModule"]
old-location: display\engfreemodule.htm
tech.root: display
ms.assetid: f5520aec-5747-4970-ba2f-06b39e4f43f2
ms.date: 12/05/2018
ms.keywords: EngFreeModule, EngFreeModule function [Display Devices], display.engfreemodule, gdifncs_23d84e6d-60e7-43a4-af20-3234c8581190.xml, winddi/EngFreeModule
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
 - EngFreeModule
 - winddi/EngFreeModule
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-full-export-l1-1-0.dll
 - Win32k.sys
 - Ext-MS-Win-moderncore-Win32k-base-ntgdi-l1-1-0.dll
 - win32kfull.sys
 - win32kmin.sys
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - EngFreeModule
---

# EngFreeModule function


## -description

The <b>EngFreeModule</b> function unmaps a file from system memory.

## -parameters

### -param h [in]

Handle to the memory-mapped file to be freed. This handle was obtained from <a href="/windows/desktop/api/winddi/nf-winddi-engloadmodule">EngLoadModule</a> or <a href="/windows/desktop/api/winddi/nf-winddi-engloadmoduleforwrite">EngLoadModuleForWrite</a>.

## -returns

None

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engloadmodule">EngLoadModule</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engloadmoduleforwrite">EngLoadModuleForWrite</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engmapmodule">EngMapModule</a>