---
UID: NC:dxmini.PDX_BOBNEXTFIELD
title: PDX_BOBNEXTFIELD (dxmini.h)
description: The DxBobNextField callback function bobs the next field of interleaved data.
helpviewer_keywords: ["DxBobNextField","DxBobNextField callback function [Display Devices]","PDX_BOBNEXTFIELD","PDX_BOBNEXTFIELD callback","VideoMiniPort_DxApiFunctions_d95db457-005d-4eee-a110-19159f64008b.xml","display.dxbobnextfield","dxmini/DxBobNextField"]
old-location: display\dxbobnextfield.htm
tech.root: display
ms.assetid: 5daafc0c-2a6d-45e2-8403-d54cb383b3b7
ms.date: 12/05/2018
ms.keywords: DxBobNextField, DxBobNextField callback function [Display Devices], PDX_BOBNEXTFIELD, PDX_BOBNEXTFIELD callback, VideoMiniPort_DxApiFunctions_d95db457-005d-4eee-a110-19159f64008b.xml, display.dxbobnextfield, dxmini/DxBobNextField
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
 - PDX_BOBNEXTFIELD
 - dxmini/PDX_BOBNEXTFIELD
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
 - DxBobNextField
---

## -description

The <i>DxBobNextField</i> callback function bobs the next field of interleaved data.

## -parameters

### -param unnamedParam1

Points to the miniport driver's device extension.

### -param unnamedParam2

Points to a <a href="/windows/desktop/api/dxmini/ns-dxmini-ddbobnextfieldinfo">DDBOBNEXTFIELDINFO</a> structure that contains the bob information for the surface.

### -param unnamedParam3

Reserved for system use.

## -returns

<i>DxBobNextField</i> returns DX_OK if it succeeds; otherwise, it returns one of the following error values:

<a href="/windows-hardware/drivers/display/return-values-for-directdraw">DXERR_GENERIC</a>

<a href="/windows-hardware/drivers/display/return-values-for-directdraw">DXERR_OUTOFCAPS</a>

<a href="/windows-hardware/drivers/display/return-values-for-directdraw">DXERR_UNSUPPORTED</a>

## -remarks

When data is interleaved, the driver's <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_flip">DdFlip</a> function is called every other frame. This is insufficient for bob because it must be notified after every V-sync. The driver's <i>DxBobNextField</i> function is called when a V-sync does not cause a flip.

## -see-also

<a href="/windows/desktop/api/dxmini/ns-dxmini-ddbobnextfieldinfo">DDBOBNEXTFIELDINFO</a>

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_flip">DdFlip</a>
