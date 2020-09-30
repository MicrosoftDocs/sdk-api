---
UID: NF:winddi.DrvUnloadFontFile
title: DrvUnloadFontFile function (winddi.h)
description: The DrvUnloadFontFile function informs a font driver that the specified font file is no longer needed.
helpviewer_keywords: ["DrvUnloadFontFile","DrvUnloadFontFile function [Display Devices]","ddifncs_db8c3f72-5fde-4dd3-84e1-5bea9b7e530d.xml","display.drvunloadfontfile","winddi/DrvUnloadFontFile"]
old-location: display\drvunloadfontfile.htm
tech.root: display
ms.assetid: 2b4b946a-30d0-434f-ab04-73bedd6a01aa
ms.date: 12/05/2018
ms.keywords: DrvUnloadFontFile, DrvUnloadFontFile function [Display Devices], ddifncs_db8c3f72-5fde-4dd3-84e1-5bea9b7e530d.xml, display.drvunloadfontfile, winddi/DrvUnloadFontFile
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Desktop
req.target-min-winverclnt: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrvUnloadFontFile
 - winddi/DrvUnloadFontFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvUnloadFontFile
---

# DrvUnloadFontFile function


## -description

The <b>DrvUnloadFontFile</b> function informs a font driver that the specified font file is no longer needed.

## -parameters

### -param iFile

Pointer to a driver-defined value that identifies the font file to be removed. The <i>iFile</i> parameter is the value returned by <a href="/windows/desktop/api/winddi/nf-winddi-drvloadfontfile">DrvLoadFontFile</a>.

## -returns

The return value is <b>TRUE</b> if the function is successful, and <b>FALSE</b> otherwise.

## -remarks

The driver should delete all scratch files, unload all DLLs that were loaded, and free all allocated system resources at this time.

This function is required for font drivers.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvloadfontfile">DrvLoadFontFile</a>