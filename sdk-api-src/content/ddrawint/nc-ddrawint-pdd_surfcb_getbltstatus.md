---
UID: NC:ddrawint.PDD_SURFCB_GETBLTSTATUS
title: PDD_SURFCB_GETBLTSTATUS (ddrawint.h)
description: The DdGetBltStatus callback function queries the blit status of the specified surface.
helpviewer_keywords: ["DdGetBltStatus","DdGetBltStatus callback function [Display Devices]","PDD_SURFCB_GETBLTSTATUS","PDD_SURFCB_GETBLTSTATUS callback","ddfncs_b4844b94-b4ec-402e-87c3-b7d83a980963.xml","ddrawint/DdGetBltStatus","display.ddgetbltstatus"]
old-location: display\ddgetbltstatus.htm
tech.root: display
ms.assetid: 77cce7a4-a0e6-48f7-933f-a216b13ddc93
ms.date: 12/05/2018
ms.keywords: DdGetBltStatus, DdGetBltStatus callback function [Display Devices], PDD_SURFCB_GETBLTSTATUS, PDD_SURFCB_GETBLTSTATUS callback, ddfncs_b4844b94-b4ec-402e-87c3-b7d83a980963.xml, ddrawint/DdGetBltStatus, display.ddgetbltstatus
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
 - PDD_SURFCB_GETBLTSTATUS
 - ddrawint/PDD_SURFCB_GETBLTSTATUS
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
 - DdGetBltStatus
---

## -description

The <b>DdGetBltStatus</b> callback function queries the blit status of the specified surface.

## -parameters

### -param unnamedParam1

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_getbltstatusdata">DD_GETBLTSTATUSDATA</a> structure that contains the information required to perform the blit status query.

## -returns

<b>DdGetBltStatus</b> returns one of the following callback codes:

## -remarks

The blit status that the driver returns is based on the <b>dwFlags</b> member of the structure that <i>lpGetBltStatus</i> points to, as follows:

<ul>
<li>
If the flag is DDGBS_CANBLT, the driver should determine whether the surface is currently involved in a flip. If a flip is not in progress and if the hardware is otherwise capable of currently accepting a blit request, the driver should return DD_OK in the <b>ddRVal</b> member of the structure that <i>lpGetBltStatus</i> points to. If a flip is in progress or if the hardware cannot currently accept another blit request, the driver should set the <b>ddRVal</b> member to DDERR_WASSTILLDRAWING.

</li>
<li>
If the flag is DDGBS_ISBLTDONE, the driver should set <b>ddRVal</b> to DDERR_WASSTILLDRAWING if a blit is currently in progress; otherwise it should return DD_OK.

</li>
</ul>

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_getbltstatusdata">DD_GETBLTSTATUSDATA</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_blt">DdBlt</a>