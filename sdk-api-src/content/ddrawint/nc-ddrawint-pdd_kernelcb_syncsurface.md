---
UID: NC:ddrawint.PDD_KERNELCB_SYNCSURFACE
title: PDD_KERNELCB_SYNCSURFACE (ddrawint.h)
description: The DdSyncSurfaceData callback function sets and modifies surface data before it is passed to the video miniport driver.
helpviewer_keywords: ["DdSyncSurfaceData","DdSyncSurfaceData callback function [Display Devices]","PDD_KERNELCB_SYNCSURFACE","PDD_KERNELCB_SYNCSURFACE callback","ddfncs_ca658342-3cbc-446d-8089-80b1a3e2ef6d.xml","ddrawint/DdSyncSurfaceData","display.ddsyncsurfacedata"]
old-location: display\ddsyncsurfacedata.htm
tech.root: display
ms.assetid: 730e0fd4-aaae-4de7-86d5-fa2145be3cd1
ms.date: 12/05/2018
ms.keywords: DdSyncSurfaceData, DdSyncSurfaceData callback function [Display Devices], PDD_KERNELCB_SYNCSURFACE, PDD_KERNELCB_SYNCSURFACE callback, ddfncs_ca658342-3cbc-446d-8089-80b1a3e2ef6d.xml, ddrawint/DdSyncSurfaceData, display.ddsyncsurfacedata
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
 - PDD_KERNELCB_SYNCSURFACE
 - ddrawint/PDD_KERNELCB_SYNCSURFACE
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
 - DdSyncSurfaceData
---

## -description

The <i>DdSyncSurfaceData</i> callback function sets and modifies surface data before it is passed to the video miniport driver.

## -parameters

### -param unnamedParam1

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_syncsurfacedata">DD_SYNCSURFACEDATA</a> structure that contains the surface data.

## -returns

<i>DdSyncSurfaceData</i> returns one of the following callback codes:

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_syncsurfacedata">DD_SYNCSURFACEDATA</a>