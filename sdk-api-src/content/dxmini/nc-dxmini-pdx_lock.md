---
UID: NC:dxmini.PDX_LOCK
title: PDX_LOCK (dxmini.h)
description: The DxLock callback function is called when a client of the video miniport driver wants access to the frame buffer.
helpviewer_keywords: ["DxLock","DxLock callback function [Display Devices]","PDX_LOCK","PDX_LOCK callback","VideoMiniPort_DxApiFunctions_35d3fff6-f764-4dd7-a239-74dde81cdebb.xml","display.dxlock","dxmini/DxLock"]
old-location: display\dxlock.htm
tech.root: display
ms.assetid: 1eeeb68b-9098-4030-924a-634e79c3e682
ms.date: 12/05/2018
ms.keywords: DxLock, DxLock callback function [Display Devices], PDX_LOCK, PDX_LOCK callback, VideoMiniPort_DxApiFunctions_35d3fff6-f764-4dd7-a239-74dde81cdebb.xml, display.dxlock, dxmini/DxLock
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
 - PDX_LOCK
 - dxmini/PDX_LOCK
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
 - DxLock
---

## -description

The<i> DxLock</i> callback function is called when a client of the video miniport driver wants access to the frame buffer.

## -parameters

### -param unnamedParam1
Points to the miniport driver's device extension.

### -param unnamedParam2
Points to a <a href="/windows/desktop/api/dxmini/ns-dxmini-ddlockininfo">DDLOCKININFO</a> structure that contains the surface information for the lock.

### -param unnamedParam3
Points to a <a href="/windows/desktop/api/dxmini/ns-dxmini-ddlockoutinfo">DDLOCKOUTINFO</a> structure that contains the surface in the frame buffer.

## -returns

<i>DxLock</i> returns DX_OK if it succeeds; otherwise, it returns one of the following error values:

## -remarks

The <a href="/windows/desktop/api/dxmini/ns-dxmini-ddlockininfo">DDLOCKININFO</a> and <a href="/windows/desktop/api/dxmini/ns-dxmini-ddlockoutinfo">DDLOCKOUTINFO</a> structures contain surface information.

## -see-also

<a href="/windows/desktop/api/dxmini/ns-dxmini-ddlockininfo">DDLOCKININFO</a>

<a href="/windows/desktop/api/dxmini/ns-dxmini-ddlockoutinfo">DDLOCKOUTINFO</a>
