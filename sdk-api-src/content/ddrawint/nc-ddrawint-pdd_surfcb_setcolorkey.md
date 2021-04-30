---
UID: NC:ddrawint.PDD_SURFCB_SETCOLORKEY
title: PDD_SURFCB_SETCOLORKEY (ddrawint.h)
description: The DdSetColorKey callback function sets the color key value for the specified surface.
helpviewer_keywords: ["DdSetColorKey","DdSetColorKey callback function [Display Devices]","PDD_SURFCB_SETCOLORKEY","PDD_SURFCB_SETCOLORKEY callback","ddfncs_d15b9bba-6ff4-441e-8bbe-f23e85de8e32.xml","ddrawint/DdSetColorKey","display.ddsetcolorkey"]
old-location: display\ddsetcolorkey.htm
tech.root: display
ms.assetid: 4b4ee889-15c8-4a7c-a9d8-adab27b271dd
ms.date: 12/05/2018
ms.keywords: DdSetColorKey, DdSetColorKey callback function [Display Devices], PDD_SURFCB_SETCOLORKEY, PDD_SURFCB_SETCOLORKEY callback, ddfncs_d15b9bba-6ff4-441e-8bbe-f23e85de8e32.xml, ddrawint/DdSetColorKey, display.ddsetcolorkey
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
 - PDD_SURFCB_SETCOLORKEY
 - ddrawint/PDD_SURFCB_SETCOLORKEY
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
 - DdSetColorKey
---

## -description

The <i>DdSetColorKey</i> callback function sets the color key value for the specified surface.

## -parameters

### -param unnamedParam1

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_setcolorkeydata">DD_SETCOLORKEYDATA</a> structure that contains the information required to set the color key for the specified surface.

## -returns

<i>DdSetColorKey</i> returns one of the following callback codes:

## -remarks

<i>DdSetColorKey</i> sets the source or destination color key for the specified surface. Typically, this callback is implemented only for drivers that support overlays with color key capabilities.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_setcolorkeydata">DD_SETCOLORKEYDATA</a>