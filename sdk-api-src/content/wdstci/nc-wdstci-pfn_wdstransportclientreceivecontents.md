---
UID: NC:wdstci.PFN_WdsTransportClientReceiveContents
title: PFN_WdsTransportClientReceiveContents (wdstci.h)
description: The PFN_WdsTransportClientReceiveContents callback is used by the multicast client to indicate that a block of data is ready to be used.
helpviewer_keywords: ["PFN_WdsTransportClientReceiveContents","PFN_WdsTransportClientReceiveContents callback","PFN_WdsTransportClientReceiveContents callback function [Windows Deployment Services]","wds.pfn_wdstransportclientreceivecontents","wdstci/PFN_WdsTransportClientReceiveContents"]
old-location: wds\pfn_wdstransportclientreceivecontents.htm
tech.root: wds
ms.assetid: 3a1cd9bb-c0da-4d66-9338-1f284fc15499
ms.date: 12/05/2018
ms.keywords: PFN_WdsTransportClientReceiveContents, PFN_WdsTransportClientReceiveContents callback, PFN_WdsTransportClientReceiveContents callback function [Windows Deployment Services], wds.pfn_wdstransportclientreceivecontents, wdstci/PFN_WdsTransportClientReceiveContents
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
 - PFN_WdsTransportClientReceiveContents
 - wdstci/PFN_WdsTransportClientReceiveContents
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
 - PFN_WdsTransportClientReceiveContents
---

# PFN_WdsTransportClientReceiveContents callback function


## -description

The PFN_WdsTransportClientReceiveContents callback is used by the multicast client to indicate that a block of data is ready to be used.

## -parameters

### -param hSessionKey [in]

The handle belonging to the session that is being started.

### -param pCallerData [in]

Pointer to the user data for this session.  This data was specified in the call to the <a href="/windows/desktop/api/wdstci/nf-wdstci-wdstransportclientstartsession">WdsTransportClientStartSession</a> function.

### -param pContents

### -param ulSize [in]

The size of the data in <i>pCallerData</i>.

### -param pullContentOffset

#### - pContentOffset [in]

The offset in the data stream where this block of data starts.  


#### - pMetadata [in]

Pointer to the buffer location  that has received the content. The size of this buffer in bytes is given by <i>ulSize</i>.