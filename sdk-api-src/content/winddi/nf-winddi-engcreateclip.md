---
UID: NF:winddi.EngCreateClip
title: EngCreateClip function (winddi.h)
description: The EngCreateClip function creates a CLIPOBJ structure that the driver uses in callbacks.
helpviewer_keywords: ["EngCreateClip","EngCreateClip function [Display Devices]","display.engcreateclip","gdifncs_e1faed88-1f89-49c2-871e-097e56db1a10.xml","winddi/EngCreateClip"]
old-location: display\engcreateclip.htm
tech.root: display
ms.assetid: 719b006f-1eb0-41c6-8b88-c8241a394abe
ms.date: 12/05/2018
ms.keywords: EngCreateClip, EngCreateClip function [Display Devices], display.engcreateclip, gdifncs_e1faed88-1f89-49c2-871e-097e56db1a10.xml, winddi/EngCreateClip
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
 - EngCreateClip
 - winddi/EngCreateClip
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
 - EngCreateClip
---

# EngCreateClip function


## -description

The <b>EngCreateClip</b> function creates a <a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a> structure that the driver uses in callbacks.



## -returns

The return value is a pointer to the newly-created CLIPOBJ structure if the function succeeds. Otherwise, it is <b>NULL</b>.

## -remarks

The CLIPOBJ structure created by <b>EngCreateClip</b> allows GDI to directly access banked frame buffers. The structure must be initialized by the driver so that the <b>iDComplexity</b> member of the CLIPOBJ structure is set to DC_TRIVIAL or DC_RECT. If the <b>iDComplexity</b> member is set to DC_RECT, the driver can set the <b>rclBounds</b> member of CLIPOBJ to the extent of the frame buffer bank. The driver must delete this CLIPOBJ structure using <a href="/windows/desktop/api/winddi/nf-winddi-engdeleteclip">EngDeleteClip</a>.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engdeleteclip">EngDeleteClip</a>
