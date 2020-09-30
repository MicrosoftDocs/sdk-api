---
UID: NF:wdstci.WdsTransportClientCompleteReceive
title: WdsTransportClientCompleteReceive function (wdstci.h)
description: Indicates that all processing on a block of data is finished, and that the multicast client may purge this block of data from its cache to make room for further receives.
helpviewer_keywords: ["WdsTransportClientCompleteReceive","WdsTransportClientCompleteReceive function [Windows Deployment Services]","wds.wdstransportclientcompletereceive","wdstci/WdsTransportClientCompleteReceive"]
old-location: wds\wdstransportclientcompletereceive.htm
tech.root: wds
ms.assetid: 1c5cdd44-e818-43ef-aaba-60a01660f7cf
ms.date: 12/05/2018
ms.keywords: WdsTransportClientCompleteReceive, WdsTransportClientCompleteReceive function [Windows Deployment Services], wds.wdstransportclientcompletereceive, wdstci/WdsTransportClientCompleteReceive
req.header: wdstci.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wdstptc.lib
req.dll: Wdstptc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WdsTransportClientCompleteReceive
 - wdstci/WdsTransportClientCompleteReceive
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wdstptc.dll
api_name:
 - WdsTransportClientCompleteReceive
---

# WdsTransportClientCompleteReceive function


## -description

Indicates that all processing on a block of data is finished, and that the multicast client may purge this block of data from its cache to make room for further receives.

## -parameters

### -param hSessionKey [in]

Unique handle returned by the call to <a href="/windows/desktop/api/wdstci/nf-wdstci-wdstransportclientinitializesession">WdsTransportClientInitializeSession</a>.

### -param ulSize [in]

The size of the block being released.

### -param pullOffset [in]

The offset of the block being released.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

## -remarks

There must be one call to <b>WdsTransportClientCompleteReceive</b> for each call to the <a href="/windows/desktop/api/wdstci/nc-wdstci-pfn_wdstransportclientreceivecontents">PFN_WdsTransportClientReceiveContents</a> callback that the consumer receives.  The length and offset parameters of this function call must match those provided in the receive contents callback.  Failure to call this function will result in a stall in the multicast client once it hits the cache limit specified by the <i>ulCacheSize</i> of the <a href="/windows/desktop/api/wdstci/ns-wdstci-wds_transportclient_request">WDS_TRANSPORTCLIENT_REQUEST</a> structure passed to <a href="/windows/desktop/api/wdstci/nf-wdstci-wdstransportclientinitializesession">WdsTransportClientInitializeSession</a>.