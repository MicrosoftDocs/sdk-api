---
UID: NC:dxmini.PDX_GETIRQINFO
title: PDX_GETIRQINFO (dxmini.h)
description: The DxGetIRQInfo callback function indicates that the driver manages the interrupt request.
helpviewer_keywords: ["DxGetIRQInfo","DxGetIRQInfo callback function [Display Devices]","PDX_GETIRQINFO","PDX_GETIRQINFO callback","VideoMiniPort_DxApiFunctions_1e787efc-ec94-4fa0-bc13-22142c16cc8d.xml","display.dxgetirqinfo","dxmini/DxGetIRQInfo"]
old-location: display\dxgetirqinfo.htm
tech.root: display
ms.assetid: bc7463ab-1cb1-4ce5-a929-1513507a16ff
ms.date: 12/05/2018
ms.keywords: DxGetIRQInfo, DxGetIRQInfo callback function [Display Devices], PDX_GETIRQINFO, PDX_GETIRQINFO callback, VideoMiniPort_DxApiFunctions_1e787efc-ec94-4fa0-bc13-22142c16cc8d.xml, display.dxgetirqinfo, dxmini/DxGetIRQInfo
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
 - PDX_GETIRQINFO
 - dxmini/PDX_GETIRQINFO
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
 - DxGetIRQInfo
---

## -description

The<i> DxGetIRQInfo</i> callback function indicates that the driver manages the interrupt request.

## -parameters

### -param unnamedParam1
Points to the miniport driver's device extension.

### -param unnamedParam2
Reserved for system use.

### -param unnamedParam3
Points to a <a href="/windows/desktop/api/dxmini/ns-dxmini-ddgetirqinfo">DDGETIRQINFO</a> structure that contains the interrupt request information.

## -returns

<i>DxGetIrqInfo</i> returns DX_OK if it succeeds; otherwise, it returns one of the following error values:

## -remarks

Because the miniport driver must always manage the IRQ, this function must always set the <b>dwFlags</b> member of the DDGETIRQINFO structure at <i>GetIrqInfo</i> to IRQINFO_HANDLED. If any other flag is set, this function will fail.

## -see-also

<a href="/windows/desktop/api/dxmini/ns-dxmini-ddgetirqinfo">DDGETIRQINFO</a>
