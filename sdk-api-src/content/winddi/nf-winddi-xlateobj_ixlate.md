---
UID: NF:winddi.XLATEOBJ_iXlate
title: XLATEOBJ_iXlate function (winddi.h)
description: The XLATEOBJ_iXlate function translates a color index of the source palette to the closest index in the destination palette.
helpviewer_keywords: ["XLATEOBJ_iXlate","XLATEOBJ_iXlate function [Display Devices]","display.xlateobj_ixlate","gdifncs_c1ca950a-fb95-47ae-936a-857ffc47c027.xml","winddi/XLATEOBJ_iXlate"]
old-location: display\xlateobj_ixlate.htm
tech.root: display
ms.assetid: 1506efcb-d4fa-4120-89ba-5aca0f3c7f97
ms.date: 12/05/2018
ms.keywords: XLATEOBJ_iXlate, XLATEOBJ_iXlate function [Display Devices], display.xlateobj_ixlate, gdifncs_c1ca950a-fb95-47ae-936a-857ffc47c027.xml, winddi/XLATEOBJ_iXlate
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
 - XLATEOBJ_iXlate
 - winddi/XLATEOBJ_iXlate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-common-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - XLATEOBJ_iXlate
---

# XLATEOBJ_iXlate function


## -description

The <b>XLATEOBJ_iXlate</b> function translates a color index of the source palette to the closest index in the destination palette.

## -parameters

### -param pxlo

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-xlateobj">XLATEOBJ</a> structure that defines the source palette.

### -param iColor

Specifies the color index to be translated.

## -returns

The return value is an index into the destination palette if the function is successful. If the function fails, -1 is returned.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-xlateobj">XLATEOBJ</a>