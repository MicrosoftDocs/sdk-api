---
UID: NF:winddi.DrvGetDirectDrawInfo
title: DrvGetDirectDrawInfo function (winddi.h)
description: The DrvGetDirectDrawInfo function returns the capabilities of the graphics hardware.
helpviewer_keywords: ["DrvGetDirectDrawInfo","DrvGetDirectDrawInfo function [Display Devices]","ddfncs_bebc9a48-6664-4b23-908f-a4c586e79f63.xml","display.drvgetdirectdrawinfo","winddi/DrvGetDirectDrawInfo"]
old-location: display\drvgetdirectdrawinfo.htm
tech.root: display
ms.assetid: c6068572-bd73-4faa-b085-9608ebc450ea
ms.date: 12/05/2018
ms.keywords: DrvGetDirectDrawInfo, DrvGetDirectDrawInfo function [Display Devices], ddfncs_bebc9a48-6664-4b23-908f-a4c586e79f63.xml, display.drvgetdirectdrawinfo, winddi/DrvGetDirectDrawInfo
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
 - DrvGetDirectDrawInfo
 - winddi/DrvGetDirectDrawInfo
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
 - DrvGetDirectDrawInfo
---

# DrvGetDirectDrawInfo function


## -description

The <b>DrvGetDirectDrawInfo</b> function returns the capabilities of the graphics hardware.

## -parameters

### -param dhpdev

Handle to the <a href="/windows-hardware/drivers/">PDEV</a> returned by the driver's <a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a> routine.

### -param pHalInfo

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_halinfo">DD_HALINFO</a> structure in which the driver should return the hardware capabilities that it supports.

### -param pdwNumHeaps

Points to the location in which the driver should return the number of VIDEOMEMORY structures pointed to by <i>pvmList</i>.

### -param pvmList

Points to an array of <a href="/windows/desktop/api/ddrawint/ns-ddrawint-videomemory">VIDEOMEMORY</a> structures in which the driver should return information about each display memory chunk that it controls. The driver should ignore this parameter when it is <b>NULL</b>.

### -param pdwNumFourCCCodes

Points to the location in which the driver should return the number of DWORDs pointed to by <i>pdwFourCC</i>.

### -param pdwFourCC

Points to an array of DWORDs in which the driver should return information about each <a href="/windows-hardware/drivers/">FOURCC</a> that it supports. The driver should ignore this parameter when it is <b>NULL</b>.

## -returns

<b>DrvGetDirectDrawInfo</b> returns <b>TRUE</b> if it succeeds; otherwise, it returns <b>FALSE</b>.

## -remarks

The driver's <b>DrvGetDirectDrawInfo</b> routine should do the following:

<ul>
<li>When <i>pvmList</i> and <i>pdwFourCC</i> are <b>NULL</b>:<ol>
<li>Reserve offscreen display memory for DirectDraw use.</li>
<li>Write the number of driver display memory heaps and supported FOURCCs in <i>pdwNumHeaps</i> and <i>pdwNumFourCC</i>, respectively.</li>
</ol>
</li>
<li>When <i>pvmList</i> and <i>pdwFourCC</i> are not <b>NULL</b>:<ol>
<li>Write the number of driver display memory heaps and supported FOURCCs in <i>pdwNumHeaps</i> and <i>pdwNumFourCC</i>, respectively.</li>
<li>For each <a href="/windows/desktop/api/ddrawint/ns-ddrawint-videomemory">VIDEOMEMORY</a> structure in the list to which <i>pvmList</i> points, fill in the appropriate members to describe a particular chunk of display memory. The list of structures provides DirectDraw with a complete description of the driver's offscreen memory.</li>
</ol>
</li>
<li>Initialize the members of the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_halinfo">DD_HALINFO</a> structure with driver-specific information as follows:<ol>
<li>Initialize the appropriate members of the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-videomemoryinfo">VIDEOMEMORYINFO</a> structure in <i>vmiData</i> to describe the general characteristics of the display's memory.</li>
<li>Initialize the appropriate members of the <a href="/windows/desktop/api/ddrawi/ns-ddrawi-ddcorecaps">DDCORECAPS</a> structure in <b>ddCaps</b> to describe the capabilities of the hardware.</li>
<li>If the driver implements a <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverinfo">DdGetDriverInfo</a> function, set <b>GetDriverInfo</b> to point to it and set <b>dwFlags</b> to DDHALINFO_GETDRIVERINFOSET.</li>
</ol>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_halinfo">DD_HALINFO</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverinfo">DdGetDriverInfo</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvenabledirectdraw">DrvEnableDirectDraw</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-videomemory">VIDEOMEMORY</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-videomemoryinfo">VIDEOMEMORYINFO</a>