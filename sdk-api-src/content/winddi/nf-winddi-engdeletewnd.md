---
UID: NF:winddi.EngDeleteWnd
title: EngDeleteWnd function (winddi.h)
description: The EngDeleteWnd function deletes a WNDOBJ structure.
helpviewer_keywords: ["EngDeleteWnd","EngDeleteWnd function [Display Devices]","display.engdeletewnd","gdifncs_7a608897-cca5-45c9-94ea-afa7d3f6ed6a.xml","winddi/EngDeleteWnd"]
old-location: display\engdeletewnd.htm
tech.root: display
ms.assetid: bc6b3a61-18f6-4c7a-b6cb-a3f2dc4f6a36
ms.date: 12/05/2018
ms.keywords: EngDeleteWnd, EngDeleteWnd function [Display Devices], display.engdeletewnd, gdifncs_7a608897-cca5-45c9-94ea-afa7d3f6ed6a.xml, winddi/EngDeleteWnd
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
 - EngDeleteWnd
 - winddi/EngDeleteWnd
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
 - EngDeleteWnd
---

# EngDeleteWnd function


## -description

The <b>EngDeleteWnd</b> function deletes a <a href="/windows/desktop/api/winddi/ns-winddi-wndobj">WNDOBJ</a> structure.

## -parameters

### -param pwo

Pointer to the WNDOBJ structure to be deleted.

## -returns

None

## -remarks

Because deleting a window object involves locking window resources, <b>EngDeleteWnd</b> should be called only in the context of the WNDOBJ_SETUP escape in <a href="/windows/desktop/api/winddi/nf-winddi-drvescape">DrvEscape</a>, or from an <a href="/windows-hardware/drivers/">MCD</a> or <a href="/windows-hardware/drivers/">ICD</a> escape.

A driver can call <b>EngDeleteWnd</b> to remove its WNDOBJ structure associated with a window regardless of whether the window continues to exist. This is useful when the driver is being dynamically unloaded by the system while the associated window still exists.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engcreatewnd">EngCreateWnd</a>



<a href="/windows/desktop/api/winddi/ns-winddi-wndobj">WNDOBJ</a>