---
UID: NC:ddrawint.PDD_VPORTCB_WAITFORSYNC
title: PDD_VPORTCB_WAITFORSYNC (ddrawint.h)
description: The DdVideoPortWaitForSync callback function waits until the next vertical synch occurs.
helpviewer_keywords: ["DdVideoPortWaitForSync","DdVideoPortWaitForSync callback function [Display Devices]","PDD_VPORTCB_WAITFORSYNC","PDD_VPORTCB_WAITFORSYNC callback","ddfncs_11b0544a-9115-4b1f-ab6a-13b870a16ecc.xml","ddrawint/DdVideoPortWaitForSync","display.ddvideoportwaitforsync"]
old-location: display\ddvideoportwaitforsync.htm
tech.root: display
ms.assetid: 0834f49b-89c4-47cc-b591-d2b90d21ee72
ms.date: 12/05/2018
ms.keywords: DdVideoPortWaitForSync, DdVideoPortWaitForSync callback function [Display Devices], PDD_VPORTCB_WAITFORSYNC, PDD_VPORTCB_WAITFORSYNC callback, ddfncs_11b0544a-9115-4b1f-ab6a-13b870a16ecc.xml, ddrawint/DdVideoPortWaitForSync, display.ddvideoportwaitforsync
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
 - PDD_VPORTCB_WAITFORSYNC
 - ddrawint/PDD_VPORTCB_WAITFORSYNC
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
 - DdVideoPortWaitForSync
---

## -description

The <i>DdVideoPortWaitForSync</i> callback function waits until the next vertical synch occurs.

## -parameters

### -param unnamedParam1

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_waitforvportsyncdata">DD_WAITFORVPORTSYNCDATA</a> structure that contains the information required for the driver to synchronize the VPE object.

## -returns

<i>DdVideoPortWaitForSync</i> returns one of the following callback codes:

## -remarks

If the condition on which the driver is waiting does not occur before the number of milliseconds specified in the  <b>dwTimeOut</b> member of the DD_WAITFORVPORTSYNCDATA structure at <i>lpWaitForSync</i> has elapsed, the driver should set the <b>ddRVal</b> member of <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_waitforvportsyncdata">DD_WAITFORVPORTSYNCDATA</a> to DDERR_VIDEONOTACTIVE and return DDHAL_DRIVER_HANDLED.

The driver must specify its own time-out criteria when <b>dwTimeOut</b> is zero.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_waitforvportsyncdata">DD_WAITFORVPORTSYNCDATA</a>