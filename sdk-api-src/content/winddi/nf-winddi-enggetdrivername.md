---
UID: NF:winddi.EngGetDriverName
title: EngGetDriverName function (winddi.h)
description: The EngGetDriverName function returns the name of the driver's DLL.
helpviewer_keywords: ["EngGetDriverName","EngGetDriverName function [Display Devices]","display.enggetdrivername","gdifncs_e0da975e-1a7f-4f28-a38b-be0966f3b0c0.xml","winddi/EngGetDriverName"]
old-location: display\enggetdrivername.htm
tech.root: display
ms.assetid: 6af3aa76-ebb4-4abb-ba35-537ccae95220
ms.date: 12/05/2018
ms.keywords: EngGetDriverName, EngGetDriverName function [Display Devices], display.enggetdrivername, gdifncs_e0da975e-1a7f-4f28-a38b-be0966f3b0c0.xml, winddi/EngGetDriverName
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
 - EngGetDriverName
 - winddi/EngGetDriverName
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
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - EngGetDriverName
---

# EngGetDriverName function


## -description

The <b>EngGetDriverName</b> function returns the name of the driver's DLL.

## -parameters

### -param hdev [in]

Handle to the device. This is the GDI handle received by the driver as the <i>hdev</i> parameter for <a href="/windows/desktop/api/winddi/nf-winddi-drvcompletepdev">DrvCompletePDEV</a>.

## -returns

<b>EngGetDriverName</b> returns a pointer to the null-terminated string buffer in which the name of the driver's DLL is specified. The system obtains and stores the driver's name from the DRIVER_INFO_2 structure when the driver is first installed through the Win32 <b>AddPrinterDriver</b> routine.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-enggetprinterdatafilename">EngGetPrinterDataFileName</a>