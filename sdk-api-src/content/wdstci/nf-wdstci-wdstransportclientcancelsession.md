---
UID: NF:wdstci.WdsTransportClientCancelSession
title: WdsTransportClientCancelSession function (wdstci.h)
description: Releases the resources associated with a session in the client. (WdsTransportClientCancelSession)
helpviewer_keywords: ["WdsTransportClientCancelSession","WdsTransportClientCancelSession function [Windows Deployment Services]","wds.wdstransportclientcancelsession","wdstci/WdsTransportClientCancelSession"]
old-location: wds\wdstransportclientcancelsession.htm
tech.root: wds
ms.assetid: 96348bbf-e1b6-4889-a2a6-59d265c1a031
ms.date: 12/05/2018
ms.keywords: WdsTransportClientCancelSession, WdsTransportClientCancelSession function [Windows Deployment Services], wds.wdstransportclientcancelsession, wdstci/WdsTransportClientCancelSession
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
 - WdsTransportClientCancelSession
 - wdstci/WdsTransportClientCancelSession
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
 - WdsTransportClientCancelSession
---

# WdsTransportClientCancelSession function


## -description

Releases the resources associated with a session in the client.

## -parameters

### -param hSessionKey [in]

Unique handle returned by the call to <a href="/windows/desktop/api/wdstci/nf-wdstci-wdstransportclientinitializesession">WdsTransportClientInitializeSession</a>.  This session will eventually complete with an error code of <b>ERROR_CANCELLED</b> to the callback <a href="/windows/desktop/api/wdstci/nc-wdstci-pfn_wdstransportclientsessioncomplete">PFN_WdsTransportClientSessionComplete</a> callback.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

## -remarks

It is safe to call this function from within a callback.
