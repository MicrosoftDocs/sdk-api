---
UID: NF:winddi.EngDebugBreak
title: EngDebugBreak function (winddi.h)
description: The EngDebugBreak function causes a breakpoint in the current process to occur.
helpviewer_keywords: ["EngDebugBreak","EngDebugBreak function [Display Devices]","display.engdebugbreak","gdifncs_d6a74791-c6aa-4bf0-9f8b-8a52587a660f.xml","winddi/EngDebugBreak"]
old-location: display\engdebugbreak.htm
tech.root: display
ms.assetid: 068529cc-f614-426b-9593-bd153f5d5541
ms.date: 12/05/2018
ms.keywords: EngDebugBreak, EngDebugBreak function [Display Devices], display.engdebugbreak, gdifncs_d6a74791-c6aa-4bf0-9f8b-8a52587a660f.xml, winddi/EngDebugBreak
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
 - EngDebugBreak
 - winddi/EngDebugBreak
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
 - EngDebugBreak
---

# EngDebugBreak function


## -description

The <b>EngDebugBreak</b> function causes a breakpoint in the current process to occur.



## -returns

None

## -remarks

<b>EngDebugBreak</b> is useful for debugging drivers that are under development.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engdebugprint">EngDebugPrint</a>
