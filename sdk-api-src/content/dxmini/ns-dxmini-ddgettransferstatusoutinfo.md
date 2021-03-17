---
UID: NS:dxmini._DDGETTRANSFERSTATUSOUTINFO
title: DDGETTRANSFERSTATUSOUTINFO (dxmini.h)
description: The DDGETTRANSFERSTATUSOUTINFO structure contains the transfer status information.
helpviewer_keywords: ["*PDDGETTRANSFEROUTINFO","DDGETTRANSFERSTATUSOUTINFO","DDGETTRANSFERSTATUSOUTINFO structure [Display Devices]","PDDGETTRANSFEROUTINFO","PDDGETTRANSFEROUTINFO structure pointer [Display Devices]","Video_Structs_6471d175-cf52-4da4-b0c8-a4d7b96a0bea.xml","display.ddgettransferstatusoutinfo","dxmini/DDGETTRANSFERSTATUSOUTINFO","dxmini/PDDGETTRANSFEROUTINFO"]
old-location: display\ddgettransferstatusoutinfo.htm
tech.root: display
ms.assetid: 593a42be-e1e9-41e5-a006-1513c5aa5226
ms.date: 12/05/2018
ms.keywords: '*PDDGETTRANSFEROUTINFO, DDGETTRANSFERSTATUSOUTINFO, DDGETTRANSFERSTATUSOUTINFO structure [Display Devices], PDDGETTRANSFEROUTINFO, PDDGETTRANSFEROUTINFO structure pointer [Display Devices], Video_Structs_6471d175-cf52-4da4-b0c8-a4d7b96a0bea.xml, display.ddgettransferstatusoutinfo, dxmini/DDGETTRANSFERSTATUSOUTINFO, dxmini/PDDGETTRANSFEROUTINFO'
req.header: dxmini.h
req.include-header: Dxmini.h
req.target-type: Windows
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
req.typenames: DDGETTRANSFERSTATUSOUTINFO, *PDDGETTRANSFEROUTINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDGETTRANSFERSTATUSOUTINFO
 - dxmini/_DDGETTRANSFERSTATUSOUTINFO
 - PDDGETTRANSFEROUTINFO
 - dxmini/PDDGETTRANSFEROUTINFO
 - DDGETTRANSFERSTATUSOUTINFO
 - dxmini/DDGETTRANSFERSTATUSOUTINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxmini.h
api_name:
 - DDGETTRANSFERSTATUSOUTINFO
---

# DDGETTRANSFERSTATUSOUTINFO structure


## -description

The DDGETTRANSFERSTATUSOUTINFO structure contains the transfer status information.

## -struct-fields

### -field dwTransferID

Contains the transfer ID of the bus master transfer that completed. The transfer ID was originally supplied to the driver in the <b>dwTransferID</b> member of the <a href="/windows/desktop/api/dxmini/ns-dxmini-ddtransferininfo">DDTRANSFERININFO</a> structure. The driver receives a pointer to DDTRANSFERININFO in a call to its <a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_transfer">DxTransfer</a> function.

## -see-also

<a href="/windows/desktop/api/dxmini/ns-dxmini-ddtransferininfo">DDTRANSFERININFO</a>



<a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_gettransferstatus">DxGetTransferStatus</a>



<a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_transfer">DxTransfer</a>