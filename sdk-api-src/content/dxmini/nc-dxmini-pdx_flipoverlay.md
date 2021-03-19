---
UID: NC:dxmini.PDX_FLIPOVERLAY
title: PDX_FLIPOVERLAY (dxmini.h)
description: The DxFlipOverlay callback function is called when a client of the video miniport driver wants to flip the overlay or when autoflipping is enabled.
helpviewer_keywords: ["DxFlipOverlay","DxFlipOverlay callback function [Display Devices]","PDX_FLIPOVERLAY","PDX_FLIPOVERLAY callback","VideoMiniPort_DxApiFunctions_67a8d728-6197-4111-9115-597ff4311331.xml","display.dxflipoverlay","dxmini/DxFlipOverlay"]
old-location: display\dxflipoverlay.htm
tech.root: display
ms.assetid: 7674f853-e5ea-44c7-b5ed-5fd90bfa1bcb
ms.date: 12/05/2018
ms.keywords: DxFlipOverlay, DxFlipOverlay callback function [Display Devices], PDX_FLIPOVERLAY, PDX_FLIPOVERLAY callback, VideoMiniPort_DxApiFunctions_67a8d728-6197-4111-9115-597ff4311331.xml, display.dxflipoverlay, dxmini/DxFlipOverlay
req.header: dxmini.h
req.include-header: Dxmini.h
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
 - PDX_FLIPOVERLAY
 - dxmini/PDX_FLIPOVERLAY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - dxmini.h
api_name:
 - DxFlipOverlay
---

## -description

The<i> DxFlipOverlay</i> callback function is called when a client of the video miniport driver wants to flip the overlay or when autoflipping is enabled.

## -parameters

### -param unnamedParam1

Points to the miniport driver's device extension.

### -param unnamedParam2

Points to the <a href="/windows/desktop/api/dxmini/ns-dxmini-ddflipoverlayinfo">DDFLIPOVERLAYINFO</a> structure that contains the flip information for the surface.

### -param unnamedParam3

Reserved for system use.

## -returns

<i>DxFlipOverlay</i> returns DX_OK if it succeeds; otherwise, it returns one of the following error values:

## -remarks

If a hardware video port is not used and the client still wants the overlay to bob the data, the <b>dwFlags</b> member of the DDFLIPOVERLAYINFO structure at <i>FlipOverlayInfo</i> specifies the polarity of the data in the field being flipped (using the DDFLIP_EVEN or DDFLIP_ODD flags). These flags are not used when flipping a surface that is fed by a hardware video port.

## -see-also

<a href="/windows/desktop/api/dxmini/ns-dxmini-ddflipoverlayinfo">DDFLIPOVERLAYINFO</a>
