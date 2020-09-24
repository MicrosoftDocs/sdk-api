---
UID: NF:winddi.DrvEndDoc
title: DrvEndDoc function (winddi.h)
description: The DrvEndDoc function is called by GDI when it has finished sending a document to the driver for rendering.
helpviewer_keywords: ["DrvEndDoc","DrvEndDoc function [Display Devices]","ddifncs_aa6db3be-deb1-43f4-b33f-e13a8b65bf7e.xml","display.drvenddoc","winddi/DrvEndDoc"]
old-location: display\drvenddoc.htm
tech.root: display
ms.assetid: 905813fd-281d-4cc8-b006-a2d284041bb7
ms.date: 12/05/2018
ms.keywords: DrvEndDoc, DrvEndDoc function [Display Devices], ddifncs_aa6db3be-deb1-43f4-b33f-e13a8b65bf7e.xml, display.drvenddoc, winddi/DrvEndDoc
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
 - DrvEndDoc
 - winddi/DrvEndDoc
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
 - DrvEndDoc
---

# DrvEndDoc function


## -description

The <b>DrvEndDoc</b> function is called by GDI when it has finished sending a document to the driver for rendering.

## -parameters

### -param pso [in]

Caller-supplied pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure.

### -param fl [in]

Caller-supplied set of bit flags. The following flag is defined:

<table>
<tr>
<th>Flag</th>
<th>Definition</th>
</tr>
<tr>
<td>
ED_ABORTDOC

</td>
<td>
The print job is being terminated before completion.

</td>
</tr>
</table>

## -returns

If the operation succeeds, the function should return <b>TRUE</b>. Otherwise, it should call <b>SetLastError</b> to set an error code, and then return <b>FALSE</b>.

## -remarks

A <a href="/windows-hardware/drivers/print/printer-graphics-dll">printer graphics DLL</a> must provide a <b>DrvEndDoc</b> function. The function is called after the last physical page of a print job has been rendered.

Typically the function is used for sending control sequences to printer hardware, after a document has been printed, by calling GDI's <a href="/windows/desktop/api/winddi/nf-winddi-engwriteprinter">EngWritePrinter</a> function. The function can also perform internal, document-specific clean-up operations for the printer graphics DLL.

Because there is not a separate call into the printer graphics DLL when a print job is finished, the <b>DrvEndDoc</b> function must also send control sequences to the printer to end the job, if required by the printer. (In other words, there is one document per job.)

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvstartdoc">DrvStartDoc</a>