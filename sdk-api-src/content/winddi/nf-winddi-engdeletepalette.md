---
UID: NF:winddi.EngDeletePalette
title: EngDeletePalette function (winddi.h)
description: The EngDeletePalette function sends a request to GDI to delete the specified palette.
helpviewer_keywords: ["EngDeletePalette","EngDeletePalette function [Display Devices]","display.engdeletepalette","gdifncs_221095fd-b5c5-485e-9e8c-9f7a114d496d.xml","winddi/EngDeletePalette"]
old-location: display\engdeletepalette.htm
tech.root: display
ms.assetid: ebdbbb4e-aaa8-4fb7-9546-545dce803054
ms.date: 12/05/2018
ms.keywords: EngDeletePalette, EngDeletePalette function [Display Devices], display.engdeletepalette, gdifncs_221095fd-b5c5-485e-9e8c-9f7a114d496d.xml, winddi/EngDeletePalette
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
 - EngDeletePalette
 - winddi/EngDeletePalette
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
 - EngDeletePalette
---

# EngDeletePalette function


## -description

The <b>EngDeletePalette</b> function sends a request to GDI to delete the specified palette.

## -parameters

### -param hpal [in]

Handle to the palette to be deleted. This handle is supplied by <a href="/windows/desktop/api/winddi/nf-winddi-engcreatepalette">EngCreatePalette</a>.

## -returns

The return value is <b>TRUE</b> if the function is successful; otherwise, it returns <b>FALSE</b>.