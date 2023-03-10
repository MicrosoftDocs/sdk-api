---
UID: NC:dxmini.PDX_GETTRANSFERSTATUS
title: PDX_GETTRANSFERSTATUS (dxmini.h)
description: The DxGetTransferStatus callback function is used by DirectDraw to determine which hardware bus master has completed.
helpviewer_keywords: ["DxGetTransferStatus","DxGetTransferStatus callback function [Display Devices]","PDX_GETTRANSFERSTATUS","PDX_GETTRANSFERSTATUS callback","VideoMiniPort_DxApiFunctions_f0260ee6-8e6c-4ab0-bad3-8d5c2ce42488.xml","display.dxgettransferstatus","dxmini/DxGetTransferStatus"]
old-location: display\dxgettransferstatus.htm
tech.root: display
ms.assetid: e33ec8f0-2d1c-42cf-8b82-8f316f52e2a8
ms.date: 12/05/2018
ms.keywords: DxGetTransferStatus, DxGetTransferStatus callback function [Display Devices], PDX_GETTRANSFERSTATUS, PDX_GETTRANSFERSTATUS callback, VideoMiniPort_DxApiFunctions_f0260ee6-8e6c-4ab0-bad3-8d5c2ce42488.xml, display.dxgettransferstatus, dxmini/DxGetTransferStatus
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
 - PDX_GETTRANSFERSTATUS
 - dxmini/PDX_GETTRANSFERSTATUS
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
 - DxGetTransferStatus
---

## -description

The<i> DxGetTransferStatus</i> callback function is used by DirectDraw to determine which hardware bus master has completed.

## -parameters

### -param unnamedParam1
Points to the miniport driver's device extension.

### -param unnamedParam2
Reserved for system use.

### -param unnamedParam3
Points to a <a href="/windows/desktop/api/dxmini/ns-dxmini-ddgettransferstatusoutinfo">DDGETTRANSFERSTATUSOUTINFO</a> structure that contains the transfer status information.

## -returns

<i>DxGetTransferStatus</i> returns DX_OK if it succeeds; otherwise, it returns one of the following error values:

## -remarks

The driver identifies the bus master by supplying the transfer ID in the DDGETTRANSFERSTATUSOUTINFO structure. The transfer ID for each bus master is originally supplied by DirectDraw in the <b>dwTransferID</b> member of the <a href="/windows/desktop/api/dxmini/ns-dxmini-ddtransferininfo">DDTRANSFERININFO</a> structure. DirectDraw passes a pointer to DDTRANSFERININFO in its call to the driver's <a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_transfer">DxTransfer</a> function.

## -see-also

<a href="/windows/desktop/api/dxmini/ns-dxmini-ddgettransferstatusoutinfo">DDGETTRANSFERSTATUSOUTINFO</a>

<a href="/windows/desktop/api/dxmini/ns-dxmini-ddtransferininfo">DDTRANSFERININFO</a>

<a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_transfer">DxTransfer</a>
