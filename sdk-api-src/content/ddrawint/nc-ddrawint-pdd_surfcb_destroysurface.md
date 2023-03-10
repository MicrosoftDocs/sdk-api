---
UID: NC:ddrawint.PDD_SURFCB_DESTROYSURFACE
title: PDD_SURFCB_DESTROYSURFACE (ddrawint.h)
description: The DdDestroySurface callback function destroys a DirectDraw surface.
helpviewer_keywords: ["DdDestroySurface","DdDestroySurface callback function [Display Devices]","PDD_SURFCB_DESTROYSURFACE","PDD_SURFCB_DESTROYSURFACE callback","ddfncs_f6029f7a-5729-42d3-8ff6-f5e27994b133.xml","ddrawint/DdDestroySurface","display.dddestroysurface"]
old-location: display\dddestroysurface.htm
tech.root: display
ms.assetid: 90060863-02ef-49bf-820d-b3adffbc8f40
ms.date: 12/05/2018
ms.keywords: DdDestroySurface, DdDestroySurface callback function [Display Devices], PDD_SURFCB_DESTROYSURFACE, PDD_SURFCB_DESTROYSURFACE callback, ddfncs_f6029f7a-5729-42d3-8ff6-f5e27994b133.xml, ddrawint/DdDestroySurface, display.dddestroysurface
req.header: ddrawint.h
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
 - PDD_SURFCB_DESTROYSURFACE
 - ddrawint/PDD_SURFCB_DESTROYSURFACE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ddrawint.h
api_name:
 - DdDestroySurface
---

## -description

The <b>DdDestroySurface</b> callback function destroys a DirectDraw surface.

## -parameters

### -param unnamedParam1

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_destroysurfacedata">DD_DESTROYSURFACEDATA</a> structure that contains the information needed to destroy a surface.

## -returns

<b>DdDestroySurface</b> returns one of the following callback codes:

## -remarks

If DirectDraw did the memory allocation at surface creation time and the driver was not involved in the allocation, DirectDraw does not call the driver's <b>DdDestroySurface</b> function to destroy the surface. 

If the driver is performing the surface memory management itself, <b>DdDestroySurface</b> should free the surface memory and perform any other cleanup, such as freeing private data stored in the <b>dwReserved1</b> members of the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_global">DD_SURFACE_GLOBAL</a> and <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a> structures.

For a driver-managed surface, if the surface is persistent (that is, the DDSCAPS2_DONOTPERSIST flag in the <b>dwCaps2</b> member of the <a href="/previous-versions/windows/hardware/drivers/ff550292(v=vs.85)">DDSCAPS2</a> structure for the surface is not set), <b>DdDestroySurface</b> can be called with the purpose of evicting the surface from video memory. In this case, the display driver can continue to keep any private data in the <b>dwReserved1</b> members until <b>DdDestroySurface</b> is called to actually destroy the surface.

<b>DdDestroySurface</b> can be called with a disabled <a href="/windows-hardware/drivers/">PDEV</a>. PDEV is disabled or enabled by calling the display driver's <a href="/windows/desktop/api/winddi/nf-winddi-drvassertmode">DrvAssertMode</a> function. See <a href="/windows-hardware/drivers/display/managing-pdevs">Managing PDEVs</a> for more information.

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff550292(v=vs.85)">DDSCAPS2</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_destroysurfacedata">DD_DESTROYSURFACEDATA</a>



<a href="/previous-versions/windows/hardware/drivers/ff549263(v=vs.85)">DdCreateSurface</a>