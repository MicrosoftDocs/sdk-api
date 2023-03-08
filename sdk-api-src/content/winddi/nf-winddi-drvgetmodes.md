---
UID: NF:winddi.DrvGetModes
title: DrvGetModes function (winddi.h)
description: The DrvGetModes function lists the modes supported by a given device.
helpviewer_keywords: ["DrvGetModes","DrvGetModes function [Display Devices]","ddifncs_2dfdc736-13de-4235-8be3-946e0cb1ed44.xml","display.drvgetmodes","winddi/DrvGetModes"]
old-location: display\drvgetmodes.htm
tech.root: display
ms.assetid: 55ca7733-184a-4bc0-8e91-b5899073bca7
ms.date: 12/05/2018
ms.keywords: DrvGetModes, DrvGetModes function [Display Devices], ddifncs_2dfdc736-13de-4235-8be3-946e0cb1ed44.xml, display.drvgetmodes, winddi/DrvGetModes
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
 - DrvGetModes
 - winddi/DrvGetModes
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
 - DrvGetModes
---

# DrvGetModes function


## -description

The <b>DrvGetModes</b> function lists the modes supported by a given device.

## -parameters

### -param hDriver [in]

Handle to the driver for which the modes must be enumerated. This is the handle passed in the <i>hDriver</i> parameter of the <a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a> function.

### -param cjSize

Specifies the size in bytes of the buffer pointed to by <i>pdm</i>.

### -param pdm [out, optional]

Pointer to the buffer containing <a href="/windows/win32/api/wingdi/ns-wingdi-devmodew">DEVMODEW</a> structure(s) for the driver to fill in, or <b>NULL</b>.

## -returns

The driver should return the number of bytes written to the buffer if <i>pdm</i> is not <b>NULL</b>. If <i>pdm</i> is <b>NULL</b>, the driver should return the number of bytes required to hold all mode data. The driver should return zero if an error occurs.

## -remarks

This function must be implemented in all display drivers.

Window Manager dynamically loads all display drivers associated with a miniport driver (based on the <b>InstalledDisplayDrivers</b> key in the registry). Each display driver is called to retrieve the list of modes supported by that combination of loaded drivers. For example, the VGA64K display driver only returns the 64K color modes that were returned in the list of modes obtained from the miniport driver.

<b>DrvGetModes</b> can be called before there is an active PDEV.

Refer to the <i>Permedia</i> samples to see a working implementation of <b>DrvGetModes</b>.

<div class="alert"><b>Note</b>    The Microsoft Windows Driver Kit (WDK) does not contain the 3Dlabs Permedia2 (<i>3dlabs.htm</i> ) and 3Dlabs Permedia3 (<i>Perm3.htm</i>) sample display drivers. You can get these sample drivers from the Windows Server 2003 SP1 Driver Development Kit (DDK), which you can download from the <a href="/windows-hardware/drivers/devtest/">DDK - Windows Driver Development Kit</a> page of the WDHC website.</div>
<div> </div>

## -see-also

<a href="/windows/win32/api/wingdi/ns-wingdi-devmodew">DEVMODEW</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvassertmode">DrvAssertMode</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engdeviceiocontrol">EngDeviceIoControl</a>