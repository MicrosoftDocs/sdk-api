---
UID: NF:wdstptmgmt.IWdsTransportSession.RetrieveClients
title: IWdsTransportSession::RetrieveClients (wdstptmgmt.h)
description: Retrieves a collection of WDS clients joined to the transport session.
helpviewer_keywords: ["IWdsTransportSession interface [Windows Deployment Services]","RetrieveClients method","IWdsTransportSession.RetrieveClients","IWdsTransportSession::RetrieveClients","RetrieveClients","RetrieveClients method [Windows Deployment Services]","RetrieveClients method [Windows Deployment Services]","IWdsTransportSession interface","wds.iwdstransportsession_retrieveclients","wdstptmgmt/IWdsTransportSession::RetrieveClients"]
old-location: wds\iwdstransportsession_retrieveclients.htm
tech.root: wds
ms.assetid: c6e41658-8d91-4c15-8a5f-a9f43490890a
ms.date: 12/05/2018
ms.keywords: IWdsTransportSession interface [Windows Deployment Services],RetrieveClients method, IWdsTransportSession.RetrieveClients, IWdsTransportSession::RetrieveClients, RetrieveClients, RetrieveClients method [Windows Deployment Services], RetrieveClients method [Windows Deployment Services],IWdsTransportSession interface, wds.iwdstransportsession_retrieveclients, wdstptmgmt/IWdsTransportSession::RetrieveClients
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
 - IWdsTransportSession::RetrieveClients
 - wdstptmgmt/IWdsTransportSession::RetrieveClients
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
 - IWdsTransportSession.RetrieveClients
---

# IWdsTransportSession::RetrieveClients


## -description

Retrieves a collection of WDS clients joined to the transport session.

## -parameters

### -param ppWdsTransportClients [out]

A collection of objects of the <a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportclient">IWdsTransportClient</a> interface joined to the transport session.

## -returns

Standard HRESULT error values are used: S_OK for success; others for failure.

## -see-also

<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportclient">IWdsTransportClient</a>



<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportcollection">IWdsTransportCollection</a>



<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportsession">IWdsTransportSession</a>