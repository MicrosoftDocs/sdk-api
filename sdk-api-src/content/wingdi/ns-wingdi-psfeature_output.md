---
UID: NS:wingdi._PSFEATURE_OUTPUT
title: PSFEATURE_OUTPUT (wingdi.h)
description: The PSFEATURE_OUTPUT structure contains information about PostScript driver output options. This structure is used with the GET_PS_FEATURESETTING printer escape function.
helpviewer_keywords: ["*PPSFEATURE_OUTPUT","PPSFEATURE_OUTPUT","PPSFEATURE_OUTPUT structure pointer [Windows GDI]","PSFEATURE_OUTPUT","PSFEATURE_OUTPUT structure [Windows GDI]","_win32_PSFEATURE_OUTPUT_str","gdi.psfeature_output","wingdi/PPSFEATURE_OUTPUT","wingdi/PSFEATURE_OUTPUT"]
old-location: gdi\psfeature_output.htm
tech.root: xps
ms.assetid: 4ff96d45-e70e-4d80-9bab-dd1d67aee8f3
ms.date: 12/05/2018
ms.keywords: '*PPSFEATURE_OUTPUT, PPSFEATURE_OUTPUT, PPSFEATURE_OUTPUT structure pointer [Windows GDI], PSFEATURE_OUTPUT, PSFEATURE_OUTPUT structure [Windows GDI], _win32_PSFEATURE_OUTPUT_str, gdi.psfeature_output, wingdi/PPSFEATURE_OUTPUT, wingdi/PSFEATURE_OUTPUT'
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: PSFEATURE_OUTPUT, *PPSFEATURE_OUTPUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PSFEATURE_OUTPUT
 - wingdi/_PSFEATURE_OUTPUT
 - PPSFEATURE_OUTPUT
 - wingdi/PPSFEATURE_OUTPUT
 - PSFEATURE_OUTPUT
 - wingdi/PSFEATURE_OUTPUT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - PSFEATURE_OUTPUT
---

# PSFEATURE_OUTPUT structure


## -description

The <b>PSFEATURE_OUTPUT</b> structure contains information about PostScript driver output options. This structure is used with the <a href="/previous-versions/windows/desktop/legacy/dd144954(v=vs.85)">GET_PS_FEATURESETTING</a> printer escape function.

## -struct-fields

### -field bPageIndependent

<b>TRUE</b> if PostScript output is page-independent or <b>FALSE</b> if PostScript output is page-dependent.

### -field bSetPageDevice

<b>TRUE</b> if printer feature code (setpagedevice's) is included or <b>FALSE</b> if all printer feature code is suppressed.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd144954(v=vs.85)">GET_PS_FEATURESETTING</a>



<a href="/windows/desktop/printdocs/printing-and-print-spooler-structures">Print Spooler API Structures</a>



<a href="/windows/desktop/printdocs/printdocs-printing">Printing</a>