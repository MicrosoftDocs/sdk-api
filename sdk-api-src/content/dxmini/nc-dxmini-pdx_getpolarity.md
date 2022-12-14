---
UID: NC:dxmini.PDX_GETPOLARITY
title: PDX_GETPOLARITY (dxmini.h)
description: The DxGetPolarity callback function returns the polarity (even or odd) of the current field being written by the video port extensions (VPE) object.
helpviewer_keywords: ["DxGetPolarity","DxGetPolarity callback function [Display Devices]","PDX_GETPOLARITY","PDX_GETPOLARITY callback","VideoMiniPort_DxApiFunctions_caf5417f-329e-4270-a067-8a9c9634327d.xml","display.dxgetpolarity","dxmini/DxGetPolarity"]
old-location: display\dxgetpolarity.htm
tech.root: display
ms.assetid: 9bce3093-8dcd-4e91-8e20-5558f2dcce75
ms.date: 12/05/2018
ms.keywords: DxGetPolarity, DxGetPolarity callback function [Display Devices], PDX_GETPOLARITY, PDX_GETPOLARITY callback, VideoMiniPort_DxApiFunctions_caf5417f-329e-4270-a067-8a9c9634327d.xml, display.dxgetpolarity, dxmini/DxGetPolarity
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
 - PDX_GETPOLARITY
 - dxmini/PDX_GETPOLARITY
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
 - DxGetPolarity
---

## -description

The<i> DxGetPolarity</i> callback function returns the polarity (even or odd) of the current field being written by the <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> object.

## -parameters

### -param unnamedParam1

Points to the miniport driver's device extension.

### -param unnamedParam2

Points to a <a href="/windows/desktop/api/dxmini/ns-dxmini-ddgetpolarityininfo">DDGETPOLARITYININFO</a> structure that contains the VPE object from which to get the polarity information.

### -param unnamedParam3

Points to a <a href="/windows/desktop/api/dxmini/ns-dxmini-ddgetpolarityoutinfo">DDGETPOLARITYOUTINFO</a> structure that contains the polarity information for the specified VPE object.

## -returns

<i>DxGetPolarity</i> returns DX_OK if it succeeds; otherwise, it returns one of the following error values:

## -remarks

The <a href="/windows/desktop/api/dxmini/ns-dxmini-ddgetpolarityininfo">DDGETPOLARITYININFO</a> and <a href="/windows/desktop/api/dxmini/ns-dxmini-ddgetpolarityoutinfo">DDGETPOLARITYOUTINFO</a> structures contain VPE object information.

## -see-also

<a href="/windows/desktop/api/dxmini/ns-dxmini-ddgetpolarityininfo">DDGETPOLARITYININFO</a>

<a href="/windows/desktop/api/dxmini/ns-dxmini-ddgetpolarityoutinfo">DDGETPOLARITYOUTINFO</a>
