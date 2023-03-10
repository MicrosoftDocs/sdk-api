---
UID: NF:wdstci.WdsTransportClientInitializeSession
title: WdsTransportClientInitializeSession function (wdstci.h)
description: Initiates a multicast file transfer. (WdsTransportClientInitializeSession)
helpviewer_keywords: ["WdsTransportClientInitializeSession","WdsTransportClientInitializeSession function [Windows Deployment Services]","wds.wdstransportclientinitializesession","wdstci/WdsTransportClientInitializeSession"]
old-location: wds\wdstransportclientinitializesession.htm
tech.root: wds
ms.assetid: 0ece4ac8-372c-46ec-a6a1-ff1b547a85ef
ms.date: 12/05/2018
ms.keywords: WdsTransportClientInitializeSession, WdsTransportClientInitializeSession function [Windows Deployment Services], wds.wdstransportclientinitializesession, wdstci/WdsTransportClientInitializeSession
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
 - WdsTransportClientInitializeSession
 - wdstci/WdsTransportClientInitializeSession
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
 - WdsTransportClientInitializeSession
---

# WdsTransportClientInitializeSession function


## -description

Initiates a multicast file transfer.

## -parameters

### -param pSessionRequest [in]

Pointer to a <a href="/windows/desktop/api/wdstci/ns-wdstci-wds_transportclient_request">WDS_TRANSPORTCLIENT_REQUEST</a> structure that contains all the details required to initiate the multicast session.  The format of this structure is described below.

### -param pCallerData [in]

User supplied pointer that will be provided with every callback for this session.

### -param hSessionKey [out]

Buffer that will receive the address of a handle that the consumer can use to uniquely identify this session to the client.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

## -remarks

This function only sets up the session, it does not start the transfer.  To start the transfer, call <a href="/windows/desktop/api/wdstci/nf-wdstci-wdstransportclientstartsession">WdsTransportClientStartSession</a>.
