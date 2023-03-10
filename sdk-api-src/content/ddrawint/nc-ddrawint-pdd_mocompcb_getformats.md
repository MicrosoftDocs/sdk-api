---
UID: NC:ddrawint.PDD_MOCOMPCB_GETFORMATS
title: PDD_MOCOMPCB_GETFORMATS (ddrawint.h)
description: The DdMoCompGetFormats callback function indicates the uncompressed formats to which the hardware can decode the data.
helpviewer_keywords: ["DdMoCompGetFormats","DdMoCompGetFormats callback function [Display Devices]","PDD_MOCOMPCB_GETFORMATS","PDD_MOCOMPCB_GETFORMATS callback","ddfncs_bc9cd90d-e40c-4ddd-9415-3d02c4620618.xml","ddrawint/DdMoCompGetFormats","display.ddmocompgetformats"]
old-location: display\ddmocompgetformats.htm
tech.root: display
ms.assetid: 9df6473f-32a1-49bd-9ddb-2f2adec3cb45
ms.date: 12/05/2018
ms.keywords: DdMoCompGetFormats, DdMoCompGetFormats callback function [Display Devices], PDD_MOCOMPCB_GETFORMATS, PDD_MOCOMPCB_GETFORMATS callback, ddfncs_bc9cd90d-e40c-4ddd-9415-3d02c4620618.xml, ddrawint/DdMoCompGetFormats, display.ddmocompgetformats
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
 - PDD_MOCOMPCB_GETFORMATS
 - ddrawint/PDD_MOCOMPCB_GETFORMATS
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
 - DdMoCompGetFormats
---

## -description

The <b>DdMoCompGetFormats</b> callback function indicates the uncompressed formats to which the hardware can decode the data.

## -parameters

### -param unnamedParam1

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_getmocompformatsdata">DD_GETMOCOMPFORMATSDATA</a> structure that contains the uncompressed format information for the hardware.

## -returns

<b>DdMoCompGetFormats</b> returns one of the following callback codes:

## -remarks

DirectDraw drivers that support motion compensation must implement <b>DdMoCompGetFormats</b>.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_getmocompformatsdata">DD_GETMOCOMPFORMATSDATA</a>