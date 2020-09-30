---
UID: NF:wdstptmgmt.IWdsTransportNamespace.Deregister
title: IWdsTransportNamespace::Deregister (wdstptmgmt.h)
description: Deregisters the namespace on the server.
helpviewer_keywords: ["Deregister","Deregister method [Windows Deployment Services]","Deregister method [Windows Deployment Services]","IWdsTransportNamespace interface","IWdsTransportNamespace interface [Windows Deployment Services]","Deregister method","IWdsTransportNamespace.Deregister","IWdsTransportNamespace::Deregister","wds.iwdstransportnamespace_deregister","wdstptmgmt/IWdsTransportNamespace::Deregister"]
old-location: wds\iwdstransportnamespace_deregister.htm
tech.root: wds
ms.assetid: 32881121-b5aa-4ccf-9884-431dbd283e4c
ms.date: 12/05/2018
ms.keywords: Deregister, Deregister method [Windows Deployment Services], Deregister method [Windows Deployment Services],IWdsTransportNamespace interface, IWdsTransportNamespace interface [Windows Deployment Services],Deregister method, IWdsTransportNamespace.Deregister, IWdsTransportNamespace::Deregister, wds.iwdstransportnamespace_deregister, wdstptmgmt/IWdsTransportNamespace::Deregister
req.header: wdstptmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Wdstptmgmt.tlb
req.lib: 
req.dll: Wdstptmgmt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWdsTransportNamespace::Deregister
 - wdstptmgmt/IWdsTransportNamespace::Deregister
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wdstptmgmt.dll
api_name:
 - IWdsTransportNamespace.Deregister
---

# IWdsTransportNamespace::Deregister


## -description

Deregisters the namespace on the server.

## -parameters

### -param bTerminateSessions

A boolean value indicating if sessions should be terminated.

## -returns

Standard HRESULT error values are used: S_OK for success; others for failure.

## -see-also

<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportnamespace">IWdsTransportNamespace</a>