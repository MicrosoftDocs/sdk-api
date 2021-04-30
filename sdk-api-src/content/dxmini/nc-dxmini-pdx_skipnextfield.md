---
UID: NC:dxmini.PDX_SKIPNEXTFIELD
title: PDX_SKIPNEXTFIELD (dxmini.h)
description: The DxSkipNextField callback function is called when the next field needs to be skipped or reenabled.
helpviewer_keywords: ["DxSkipNextField","DxSkipNextField callback function [Display Devices]","PDX_SKIPNEXTFIELD","PDX_SKIPNEXTFIELD callback","VideoMiniPort_DxApiFunctions_417d791c-4050-4c35-aecb-bbf62e8a3e2f.xml","display.dxskipnextfield","dxmini/DxSkipNextField"]
old-location: display\dxskipnextfield.htm
tech.root: display
ms.assetid: da19c8dc-fef5-41e6-b032-2a0ae05a73da
ms.date: 12/05/2018
ms.keywords: DxSkipNextField, DxSkipNextField callback function [Display Devices], PDX_SKIPNEXTFIELD, PDX_SKIPNEXTFIELD callback, VideoMiniPort_DxApiFunctions_417d791c-4050-4c35-aecb-bbf62e8a3e2f.xml, display.dxskipnextfield, dxmini/DxSkipNextField
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
 - PDX_SKIPNEXTFIELD
 - dxmini/PDX_SKIPNEXTFIELD
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
 - DxSkipNextField
---

## -description

The<i> DxSkipNextField</i> callback function is called when the next field needs to be skipped or reenabled.

## -parameters

### -param unnamedParam1
Points to the miniport driver's device extension.

### -param unnamedParam2
Points to a <a href="/windows/desktop/api/dxmini/ns-dxmini-ddskipnextfieldinfo">DDSKIPNEXTFIELDINFO</a> structure that contains the skip information for the <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> object.

### -param unnamedParam3
Reserved for system use.

## -returns

<i>DxSkipNextField</i> returns DX_OK if it succeeds; otherwise, it returns one of the following error values:

## -remarks

If the <b>dwSkipFlags</b> member of the DDSKIPNEXTFIELDINFO structure at <i>SkipNextFieldInfo</i> is DDSKIP_SKIPNEXT, the following field should be skipped. If the vertical blanking interval (VBI) height is greater than zero, only the video data should be skipped (not the VBI data). If <b>dwSkipFlags</b> is set to DDSKIP_ENABLENEXT, the next field should be restored.

## -see-also

<a href="/windows/desktop/api/dxmini/ns-dxmini-ddskipnextfieldinfo">DDSKIPNEXTFIELDINFO</a>
