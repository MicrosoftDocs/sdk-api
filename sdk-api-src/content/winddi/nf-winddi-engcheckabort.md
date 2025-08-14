---
UID: NF:winddi.EngCheckAbort
title: EngCheckAbort function (winddi.h)
description: The EngCheckAbort function enables a printer graphics DLL to determine if a print job should be terminated.
helpviewer_keywords: ["EngCheckAbort","EngCheckAbort function [Display Devices]","display.engcheckabort","gdifncs_2d8e7bbc-f9b8-4a8b-bfd8-f9a9b93808ef.xml","winddi/EngCheckAbort"]
old-location: display\engcheckabort.htm
tech.root: display
ms.assetid: 0d117983-912b-4b77-8631-f801b914c769
ms.date: 12/05/2018
ms.keywords: EngCheckAbort, EngCheckAbort function [Display Devices], display.engcheckabort, gdifncs_2d8e7bbc-f9b8-4a8b-bfd8-f9a9b93808ef.xml, winddi/EngCheckAbort
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
 - EngCheckAbort
 - winddi/EngCheckAbort
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
 - EngCheckAbort
---

# EngCheckAbort function


## -description

The <b>EngCheckAbort</b> function enables a printer graphics DLL to determine if a print job should be terminated.

## -parameters

### -param pso

Caller-supplied pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure, previously received from GDI.

## -returns

If the print job should be terminated, the function returns <b>TRUE</b>. If the print job should not be terminated, or if <i>pso</i> does not point to a valid SURFOBJ structure, the function returns <b>FALSE</b>.

## -remarks

A <a href="/windows-hardware/drivers/print/printer-graphics-dll">printer graphics DLL</a> should call <b>EngCheckAbort</b> from within any graphics DDI function that takes more than five seconds to execute. If the print job should be terminated, the printer graphics DLL should stop its current operation and return to GDI, specifying a return value of <b>FALSE</b> for the graphics DDI function that called <b>EngCheckAbort</b>.