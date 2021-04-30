---
UID: NC:ddrawint.PDD_SURFCB_ADDATTACHEDSURFACE
title: PDD_SURFCB_ADDATTACHEDSURFACE (ddrawint.h)
description: The DdAddAttachedSurface callback function attaches a surface to another surface.
helpviewer_keywords: ["DdAddAttachedSurface","DdAddAttachedSurface callback function [Display Devices]","PDD_SURFCB_ADDATTACHEDSURFACE","PDD_SURFCB_ADDATTACHEDSURFACE callback","ddfncs_b7f5d56d-95b7-4b79-8d20-9ab663582dd2.xml","ddrawint/DdAddAttachedSurface","display.ddaddattachedsurface"]
old-location: display\ddaddattachedsurface.htm
tech.root: display
ms.assetid: 53f146e6-f521-4c95-b98b-0e8acb994c9d
ms.date: 12/05/2018
ms.keywords: DdAddAttachedSurface, DdAddAttachedSurface callback function [Display Devices], PDD_SURFCB_ADDATTACHEDSURFACE, PDD_SURFCB_ADDATTACHEDSURFACE callback, ddfncs_b7f5d56d-95b7-4b79-8d20-9ab663582dd2.xml, ddrawint/DdAddAttachedSurface, display.ddaddattachedsurface
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
 - PDD_SURFCB_ADDATTACHEDSURFACE
 - ddrawint/PDD_SURFCB_ADDATTACHEDSURFACE
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
 - DdAddAttachedSurface
---

## -description

The <b>DdAddAttachedSurface</b> callback function attaches a surface to another surface.

## -parameters

### -param unnamedParam1

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_addattachedsurfacedata">DD_ADDATTACHEDSURFACEDATA</a> structure that contains information required for the driver to perform the attachment.

## -returns

<b>DdAddAttachedSurface</b> returns one of the following callback codes:

## -remarks

<b>DdAddAttachedSurface</b> can be optionally implemented in DirectDraw drivers.

The driver should update any internal surface state it keeps to reflect the attachment.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_addattachedsurfacedata">DD_ADDATTACHEDSURFACEDATA</a>