---
UID: NF:winddi.DrvQueryDriverInfo
title: DrvQueryDriverInfo function (winddi.h)
description: The DrvQueryDriverInfo function returns requested driver-specific information.
helpviewer_keywords: ["DrvQueryDriverInfo","DrvQueryDriverInfo function [Display Devices]","ddifncs_be744729-bfb4-4c25-9f6b-e8896e6ecac5.xml","display.drvquerydriverinfo","winddi/DrvQueryDriverInfo"]
old-location: display\drvquerydriverinfo.htm
tech.root: display
ms.assetid: 94691c91-f6e9-4f48-8da2-bde5354ed94c
ms.date: 12/05/2018
ms.keywords: DrvQueryDriverInfo, DrvQueryDriverInfo function [Display Devices], ddifncs_be744729-bfb4-4c25-9f6b-e8896e6ecac5.xml, display.drvquerydriverinfo, winddi/DrvQueryDriverInfo
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
 - DrvQueryDriverInfo
 - winddi/DrvQueryDriverInfo
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
 - DrvQueryDriverInfo
---

# DrvQueryDriverInfo function


## -description

The <b>DrvQueryDriverInfo</b> function returns requested driver-specific information.

## -parameters

### -param dwMode

Caller-supplied constant value, as indicated in the following table.

<table>
<tr>
<th>Value</th>
<th>Definition</th>
</tr>
<tr>
<td>
DRVQUERY_USERMODE

</td>
<td>
The caller is querying whether the driver executes in user mode or in kernel mode.

</td>
</tr>
</table>

### -param pBuffer [out]

Caller-supplied pointer to a buffer to receive requested information. The function must supply the following information:

<table>
<tr>
<th><i>dwMode</i> Value</th>
<th><i>pBuffer</i> Size</th>
<th>Value supplied by <b>DrvQueryDriverInfo</b></th>
</tr>
<tr>
<td>
DRVQUERY_USERMODE

</td>
<td>
One DWORD

</td>
<td>
<b>TRUE</b> if driver executes in user mode; <b>FALSE</b> otherwise.

</td>
</tr>
</table>

### -param cbBuf

Caller-supplied value representing the size, in bytes, of the buffer pointed to by <i>pBuffer</i>.

### -param pcbNeeded [out]

Caller-supplied pointer to a location to receive the minimum buffer size, in bytes, required to contain the requested information.

## -returns

If the operation succeeds, the function should return <b>TRUE</b>; otherwise it should return <b>FALSE</b>.

## -remarks

<a href="/windows-hardware/drivers/print/printer-graphics-dll">Printer graphics DLLs</a> that execute in user mode must export a <b>DrvQueryDriverInfo</b> function. If the function is not exported, the <a href="/windows-hardware/drivers/print/local-print-provider">local print provider</a> assumes the graphics DLL executes in kernel mode.