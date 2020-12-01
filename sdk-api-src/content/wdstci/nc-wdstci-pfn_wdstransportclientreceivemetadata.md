---
UID: NC:wdstci.PFN_WdsTransportClientReceiveMetadata
title: PFN_WdsTransportClientReceiveMetadata (wdstci.h)
description: PFN_WdsTransportClientReceiveMetadata is an optional callback that a consumer may register to receive metadata type information about a file. This information is provided by the content provider and is opaque to the multicast client and server.
helpviewer_keywords: ["PFN_WdsTransportClientReceiveMetadata","PFN_WdsTransportClientReceiveMetadata callback","PFN_WdsTransportClientReceiveMetadata callback function [Windows Deployment Services]","wds.pfn_wdstransportclientreceivemetadata","wdstci/PFN_WdsTransportClientReceiveMetadata"]
old-location: wds\pfn_wdstransportclientreceivemetadata.htm
tech.root: wds
ms.assetid: 9acde77b-5360-4c55-b11d-bf85e5c8d00e
ms.date: 12/05/2018
ms.keywords: PFN_WdsTransportClientReceiveMetadata, PFN_WdsTransportClientReceiveMetadata callback, PFN_WdsTransportClientReceiveMetadata callback function [Windows Deployment Services], wds.pfn_wdstransportclientreceivemetadata, wdstci/PFN_WdsTransportClientReceiveMetadata
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFN_WdsTransportClientReceiveMetadata
 - wdstci/PFN_WdsTransportClientReceiveMetadata
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wdstci.h
api_name:
 - PFN_WdsTransportClientReceiveMetadata
---

# PFN_WdsTransportClientReceiveMetadata callback function


## -description

PFN_WdsTransportClientReceiveMetadata is an optional callback that a consumer may register to receive metadata type information about a file.  This information is provided by the content provider and is opaque to the multicast client and server.

## -parameters

### -param hSessionKey [in]

The handle belonging to the session that is being started.

### -param pCallerData [in]

Pointer to the caller specific data for this session.    This data was specified in the call to <a href="/windows/desktop/api/wdstci/nf-wdstci-wdstransportclientstartsession">WdsTransportClientStartSession</a> function.

### -param pMetadata [in]

Data provided by the content provider that is associated with this object in some manner.

### -param ulSize [in]

The size of the <i>pMetadata</i> buffer in bytes.