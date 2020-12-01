---
UID: NF:wdstci.WdsTransportClientWaitForCompletion
title: WdsTransportClientWaitForCompletion function (wdstci.h)
description: Blocks until either the multicast session is complete or the specified timeout is reached.
helpviewer_keywords: ["WdsTransportClientWaitForCompletion","WdsTransportClientWaitForCompletion function [Windows Deployment Services]","wds.wdstransportclientwaitforcompletion","wdstci/WdsTransportClientWaitForCompletion"]
old-location: wds\wdstransportclientwaitforcompletion.htm
tech.root: wds
ms.assetid: b592ae66-5090-468e-a747-346f87e807e8
ms.date: 12/05/2018
ms.keywords: WdsTransportClientWaitForCompletion, WdsTransportClientWaitForCompletion function [Windows Deployment Services], wds.wdstransportclientwaitforcompletion, wdstci/WdsTransportClientWaitForCompletion
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
 - WdsTransportClientWaitForCompletion
 - wdstci/WdsTransportClientWaitForCompletion
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
 - WdsTransportClientWaitForCompletion
---

# WdsTransportClientWaitForCompletion function


## -description

Blocks until either the multicast session is complete or the specified timeout is reached.

## -parameters

### -param hSessionKey [in]

Unique handle returned by the call to <a href="/windows/desktop/api/wdstci/nf-wdstci-wdstransportclientinitializesession">WdsTransportClientInitializeSession</a>.

### -param uTimeout [in]

A timeout, in milliseconds.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.