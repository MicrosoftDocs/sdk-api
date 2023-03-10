---
UID: NF:wdstci.WdsTransportClientCloseSession
title: WdsTransportClientCloseSession function (wdstci.h)
description: Releases the resources associated with a session in the client. (WdsTransportClientCloseSession)
helpviewer_keywords: ["WdsTransportClientCloseSession","WdsTransportClientCloseSession function [Windows Deployment Services]","wds.wdstransportclientclosesession","wdstci/WdsTransportClientCloseSession"]
old-location: wds\wdstransportclientclosesession.htm
tech.root: wds
ms.assetid: 4c135502-a6be-4d5d-b6ce-34b55f6e08b0
ms.date: 12/05/2018
ms.keywords: WdsTransportClientCloseSession, WdsTransportClientCloseSession function [Windows Deployment Services], wds.wdstransportclientclosesession, wdstci/WdsTransportClientCloseSession
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
 - WdsTransportClientCloseSession
 - wdstci/WdsTransportClientCloseSession
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
 - WdsTransportClientCloseSession
---

# WdsTransportClientCloseSession function


## -description

Releases the resources associated with a session in the client.

## -parameters

### -param hSessionKey [in]

Unique handle returned by the call to <a href="/windows/desktop/api/wdstci/nf-wdstci-wdstransportclientinitializesession">WdsTransportClientInitializeSession</a>. After this handle has been used with the <b>WdsTransportClientCloseSession</b>, it cannot be used again with the <a href="/windows/desktop/api/wdstci/nf-wdstci-wdstransportclientcancelsession">WdsTransportClientCancelSession</a> function.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

## -remarks

This function does not cancel the session and callbacks  can be received until session completes.
