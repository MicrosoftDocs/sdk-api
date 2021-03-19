---
UID: NC:ddrawint.PDD_VPORTCB_DESTROYVPORT
title: PDD_VPORTCB_DESTROYVPORT (ddrawint.h)
description: The DdVideoPortDestroy callback function notifies the driver that DirectDraw has destroyed the specified VPE object.
helpviewer_keywords: ["DdVideoPortDestroy","DdVideoPortDestroy callback function [Display Devices]","PDD_VPORTCB_DESTROYVPORT","PDD_VPORTCB_DESTROYVPORT callback","ddfncs_865d04b1-c817-4000-9fdc-9e498dee679c.xml","ddrawint/DdVideoPortDestroy","display.ddvideoportdestroy"]
old-location: display\ddvideoportdestroy.htm
tech.root: display
ms.assetid: 0426eeaa-4d9a-4e5e-8550-2f7adbb26685
ms.date: 12/05/2018
ms.keywords: DdVideoPortDestroy, DdVideoPortDestroy callback function [Display Devices], PDD_VPORTCB_DESTROYVPORT, PDD_VPORTCB_DESTROYVPORT callback, ddfncs_865d04b1-c817-4000-9fdc-9e498dee679c.xml, ddrawint/DdVideoPortDestroy, display.ddvideoportdestroy
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
 - PDD_VPORTCB_DESTROYVPORT
 - ddrawint/PDD_VPORTCB_DESTROYVPORT
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
 - DdVideoPortDestroy
---

## -description

The <b>DdVideoPortDestroy</b> callback function notifies the driver that DirectDraw has destroyed the specified VPE object.

## -parameters

### -param unnamedParam1

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_destroyvportdata">DD_DESTROYVPORTDATA</a> structure that contains the information required for the driver to clean up.

## -returns

<b>DdVideoPortDestroy</b> returns one of the following callback codes:

## -remarks

<b>DdVideoPortDestroy</b> can be optionally implemented in DirectDraw drivers that support VPE.

The driver should free any memory that it allocated and associated with the specified VPE object. This includes freeing any driver-allocated memory accessed through the <b>dwReserved1</b> and <b>dwReserved2</b> members of the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_videoport_local">DD_VIDEOPORT_LOCAL</a> structure. This DD_VIDEOPORT_LOCAL structure is at the <b>lpVideoPort</b> member of the DD_DESTROYVPORTDATA structure at <i>lpDestroyVideoPort</i>.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_destroyvportdata">DD_DESTROYVPORTDATA</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_videoport_local">DD_VIDEOPORT_LOCAL</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_createvideoport">DdVideoPortCreate</a>