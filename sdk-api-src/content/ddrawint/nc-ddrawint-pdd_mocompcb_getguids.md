---
UID: NC:ddrawint.PDD_MOCOMPCB_GETGUIDS
title: PDD_MOCOMPCB_GETGUIDS (ddrawint.h)
description: The DdMoCompGetGuids callback function retrieves the number of GUIDs the driver supports.
helpviewer_keywords: ["DdMoCompGetGuids","DdMoCompGetGuids callback function [Display Devices]","PDD_MOCOMPCB_GETGUIDS","PDD_MOCOMPCB_GETGUIDS callback","ddfncs_224ee005-4c85-41cc-afcf-2958c31dfd45.xml","ddrawint/DdMoCompGetGuids","display.ddmocompgetguids"]
old-location: display\ddmocompgetguids.htm
tech.root: display
ms.assetid: 22c6a3f2-4a27-4a4b-a021-8f2be04e4f87
ms.date: 12/05/2018
ms.keywords: DdMoCompGetGuids, DdMoCompGetGuids callback function [Display Devices], PDD_MOCOMPCB_GETGUIDS, PDD_MOCOMPCB_GETGUIDS callback, ddfncs_224ee005-4c85-41cc-afcf-2958c31dfd45.xml, ddrawint/DdMoCompGetGuids, display.ddmocompgetguids
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
 - PDD_MOCOMPCB_GETGUIDS
 - ddrawint/PDD_MOCOMPCB_GETGUIDS
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
 - DdMoCompGetGuids
---

## -description

The <b>DdMoCompGetGuids</b> callback function retrieves the number of GUIDs the driver supports.

## -parameters

### -param unnamedParam1

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_getmocompguidsdata">DD_GETMOCOMPGUIDSDATA</a> structure that contains the GUID information.

## -returns

<b>DdMoCompGetGuids</b> returns one of the following callback codes:

## -remarks

DirectDraw drivers that support motion compensation must implement <b>DdMoCompGetGuids</b>.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_getmocompguidsdata">DD_GETMOCOMPGUIDSDATA</a>