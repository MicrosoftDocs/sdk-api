---
UID: NC:ddrawint.PDD_SURFCB_GETFLIPSTATUS
title: PDD_SURFCB_GETFLIPSTATUS (ddrawint.h)
description: The DdGetFlipStatus callback function determines whether the most recently requested flip on a surface has occurred.
helpviewer_keywords: ["DdGetFlipStatus","DdGetFlipStatus callback function [Display Devices]","PDD_SURFCB_GETFLIPSTATUS","PDD_SURFCB_GETFLIPSTATUS callback","ddfncs_129ef755-b85d-4f99-b62b-87124364c283.xml","ddrawint/DdGetFlipStatus","display.ddgetflipstatus"]
old-location: display\ddgetflipstatus.htm
tech.root: display
ms.assetid: ec556891-e091-4c52-a155-cb6ba8011f71
ms.date: 12/05/2018
ms.keywords: DdGetFlipStatus, DdGetFlipStatus callback function [Display Devices], PDD_SURFCB_GETFLIPSTATUS, PDD_SURFCB_GETFLIPSTATUS callback, ddfncs_129ef755-b85d-4f99-b62b-87124364c283.xml, ddrawint/DdGetFlipStatus, display.ddgetflipstatus
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
 - PDD_SURFCB_GETFLIPSTATUS
 - ddrawint/PDD_SURFCB_GETFLIPSTATUS
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
 - DdGetFlipStatus
---

## -description

The <b>DdGetFlipStatus</b> callback function determines whether the most recently requested flip on a surface has occurred.

## -parameters

### -param unnamedParam1

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_getflipstatusdata">DD_GETFLIPSTATUSDATA</a> structure that contains the information required to perform the flip status query.

## -returns

<b>DdGetFlipStatus</b> returns one of the following callback codes:

## -remarks

The driver should report its flip status based on the flag set in the <b>dwFlags</b> member of the structure that <b>lpGetFlipStatus</b> points to as follows:

<ul>
<li>
If the flag is DDGFS_CANFLIP, the driver should determine whether the surface is currently involved in a flip. If a flip or a blit is not in progress and if the hardware is otherwise capable of currently accepting a flip request, the driver should return DD_OK in <b>ddRVal</b>. If a flip is in progress or if the hardware cannot currently accept a flip request, the driver should set <b>ddRVal</b> to DDERR_WASSTILLDRAWING.

</li>
<li>
If the flag is DDGFS_ISFLIPDONE, the driver should set <b>ddRVal</b> to DDERR_WASSTILLDRAWING if a flip is currently in progress; otherwise it should return DD_OK.

</li>
</ul>

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_getflipstatusdata">DD_GETFLIPSTATUSDATA</a>