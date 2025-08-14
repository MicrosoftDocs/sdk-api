---
UID: NF:winddi.WNDOBJ_vSetConsumer
title: WNDOBJ_vSetConsumer function (winddi.h)
description: The WNDOBJ_vSetConsumer function sets a driver-defined value in the pvConsumer field of the specified WNDOBJ structure.
helpviewer_keywords: ["WNDOBJ_vSetConsumer","WNDOBJ_vSetConsumer function [Display Devices]","display.wndobj_vsetconsumer","gdifncs_759188da-41cc-45c8-845f-80d23e60e88b.xml","winddi/WNDOBJ_vSetConsumer"]
old-location: display\wndobj_vsetconsumer.htm
tech.root: display
ms.assetid: c7b550b8-1a3f-4d69-93d1-241044cb4bbd
ms.date: 12/05/2018
ms.keywords: WNDOBJ_vSetConsumer, WNDOBJ_vSetConsumer function [Display Devices], display.wndobj_vsetconsumer, gdifncs_759188da-41cc-45c8-845f-80d23e60e88b.xml, winddi/WNDOBJ_vSetConsumer
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
 - WNDOBJ_vSetConsumer
 - winddi/WNDOBJ_vSetConsumer
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
api_name:
 - WNDOBJ_vSetConsumer
---

# WNDOBJ_vSetConsumer function


## -description

The <b>WNDOBJ_vSetConsumer</b> function sets a driver-defined value in the <b>pvConsumer</b> field of the specified <a href="/windows/desktop/api/winddi/ns-winddi-wndobj">WNDOBJ</a> structure.

## -parameters

### -param pwo

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-wndobj">WNDOBJ</a> structure created by a prior call to <a href="/windows/desktop/api/winddi/nf-winddi-engcreatewnd">EngCreateWnd</a>.

### -param pvConsumer

A driver-defined value for identifying this particular WNDOBJ structure. This value overrides the previous value stored in the WNDOBJ structure.

## -returns

None

## -remarks

<b>WNDOBJ_vSetConsumer</b> should be called only by the following functions:

<ul>
<li>
Graphics DDI functions for which a WNDOBJ structure is provided.

</li>
<li>
The callback provided to GDI by a driver's call to <b>EngCreateWnd</b>.

</li>
<li>
The WNDOBJ_SETUP escape defined by <a href="/windows/desktop/api/winddi/nf-winddi-drvescape">DrvEscape</a> after a new WNDOBJ structure is created.

</li>
</ul>

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvescape">DrvEscape</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engcreatewnd">EngCreateWnd</a>



<a href="/windows/desktop/api/winddi/ns-winddi-wndobj">WNDOBJ</a>