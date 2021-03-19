---
UID: NC:ddrawint.PDD_MOCOMPCB_GETCOMPBUFFINFO
title: PDD_MOCOMPCB_GETCOMPBUFFINFO (ddrawint.h)
description: The DDMoCompGetBuffInfo callback function allows the driver to specify how many interim surfaces are required to support the specified GUID, and the size, location, and format of each of these surfaces.
helpviewer_keywords: ["DdMoCompGetBuffInfo","DdMoCompGetBuffInfo callback function [Display Devices]","PDD_MOCOMPCB_GETCOMPBUFFINFO","PDD_MOCOMPCB_GETCOMPBUFFINFO callback","ddfncs_6b92e5df-6051-4481-a2a6-bb0f4cc4fd8e.xml","ddrawint/DdMoCompGetBuffInfo","display.ddmocompgetbuffinfo"]
old-location: display\ddmocompgetbuffinfo.htm
tech.root: display
ms.assetid: 7303f80d-1b6e-401f-a9ef-cf646b716c70
ms.date: 12/05/2018
ms.keywords: DdMoCompGetBuffInfo, DdMoCompGetBuffInfo callback function [Display Devices], PDD_MOCOMPCB_GETCOMPBUFFINFO, PDD_MOCOMPCB_GETCOMPBUFFINFO callback, ddfncs_6b92e5df-6051-4481-a2a6-bb0f4cc4fd8e.xml, ddrawint/DdMoCompGetBuffInfo, display.ddmocompgetbuffinfo
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
 - PDD_MOCOMPCB_GETCOMPBUFFINFO
 - ddrawint/PDD_MOCOMPCB_GETCOMPBUFFINFO
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
 - DdMoCompGetBuffInfo
---

## -description

The <b>DDMoCompGetBuffInfo</b> callback function allows the driver to specify how many interim surfaces are required to support the specified GUID, and the size, location, and format of each of these surfaces.

## -parameters

### -param unnamedParam1

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_getmocompcompbuffdata">DD_GETMOCOMPCOMPBUFFDATA</a> structure that contains the compressed buffer information.

## -returns

<b>DDMoCompGetBuffInfo</b> returns one of the following callback codes:

## -remarks

<b>DDMoCompGetBuffInfo</b> can be optionally implemented in DirectDraw drivers. This function is required for motion compensation support.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_getmocompcompbuffdata">DD_GETMOCOMPCOMPBUFFDATA</a>