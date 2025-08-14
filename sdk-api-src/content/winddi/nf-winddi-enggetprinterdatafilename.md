---
UID: NF:winddi.EngGetPrinterDataFileName
title: EngGetPrinterDataFileName function (winddi.h)
description: The EngGetPrinterDataFileName function retrieves the string name of the printer's data file.
helpviewer_keywords: ["EngGetPrinterDataFileName","EngGetPrinterDataFileName function [Display Devices]","display.enggetprinterdatafilename","gdifncs_d69cc953-8c73-4b34-af26-61f159959fa6.xml","winddi/EngGetPrinterDataFileName"]
old-location: display\enggetprinterdatafilename.htm
tech.root: display
ms.assetid: bfc698d9-a340-49a5-97fb-0dae92ab6f2d
ms.date: 12/05/2018
ms.keywords: EngGetPrinterDataFileName, EngGetPrinterDataFileName function [Display Devices], display.enggetprinterdatafilename, gdifncs_d69cc953-8c73-4b34-af26-61f159959fa6.xml, winddi/EngGetPrinterDataFileName
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
 - EngGetPrinterDataFileName
 - winddi/EngGetPrinterDataFileName
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
 - EngGetPrinterDataFileName
---

# EngGetPrinterDataFileName function


## -description

The <b>EngGetPrinterDataFileName</b> function retrieves the string name of the printer's data file.

## -parameters

### -param hdev [in]

Handle to the device. This is the GDI handle received by the driver as the <i>hdev</i> parameter for <a href="/windows/desktop/api/winddi/nf-winddi-drvcompletepdev">DrvCompletePDEV</a>.

## -returns

<b>EngGetPrinterDataFileName</b> returns a pointer to the null-terminated string buffer in which the name of the printer's data file is specified. The system obtains and stores the printer's data file name from the DRIVER_INFO_2 structure (described in the Microsoft Windows SDK documentation) when the driver is first installed through the Microsoft Win32 <b>AddPrinterDriver</b> routine.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-enggetdrivername">EngGetDriverName</a>