---
UID: NC:wdstci.PFN_WdsTransportClientSessionComplete
title: PFN_WdsTransportClientSessionComplete (wdstci.h)
description: The PFN_WdsTransportClientSessionCompete callback is used by the client to indicate that no more callbacks will be sent to the consumer and that the session either completed successfully or encountered a non-recoverable error.
helpviewer_keywords: ["PFN_WdsTransportClientSessionComplete","PFN_WdsTransportClientSessionComplete callback","PFN_WdsTransportClientSessionComplete callback function [Windows Deployment Services]","wds.pfn_wdstransportclientsessioncomplete","wdstci/PFN_WdsTransportClientSessionComplete"]
old-location: wds\pfn_wdstransportclientsessioncomplete.htm
tech.root: wds
ms.assetid: 1c7b8137-bf74-486c-a90e-6becfec5ddc8
ms.date: 12/05/2018
ms.keywords: PFN_WdsTransportClientSessionComplete, PFN_WdsTransportClientSessionComplete callback, PFN_WdsTransportClientSessionComplete callback function [Windows Deployment Services], wds.pfn_wdstransportclientsessioncomplete, wdstci/PFN_WdsTransportClientSessionComplete
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
 - PFN_WdsTransportClientSessionComplete
 - wdstci/PFN_WdsTransportClientSessionComplete
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
 - PFN_WdsTransportClientSessionComplete
---

# PFN_WdsTransportClientSessionComplete callback function


## -description

The PFN_WdsTransportClientSessionCompete callback is used by the client to indicate that no more callbacks will be sent to the consumer and that the session either completed successfully or encountered a non-recoverable error.

## -parameters

### -param hSessionKey [in]

The handle belonging to the session that is being started.

### -param pCallerData [in]

Pointer to the caller specific data for this session.  This data was specified in the call to <a href="/windows/desktop/api/wdstci/nf-wdstci-wdstransportclientstartsession">WdsTransportClientStartSession</a> function.

### -param dwError [in]

The overall status of the file transfer.  If the session succeeded, this value will be set to <b>ERROR_SUCCESS</b>.  If the session did not succeed, the error code for the session will be set.

## -remarks

This will be the last callback a consumer receives.  The consumer will always receive this callback, even if the session is canceled.