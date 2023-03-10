---
UID: NF:wdstptmgmt.IWdsTransportContent.RetrieveSessions
title: IWdsTransportContent::RetrieveSessions (wdstptmgmt.h)
description: Retrieves a collection of active transport sessions associated with this content.
helpviewer_keywords: ["IWdsTransportContent interface [Windows Deployment Services]","RetrieveSessions method","IWdsTransportContent.RetrieveSessions","IWdsTransportContent::RetrieveSessions","RetrieveSessions","RetrieveSessions method [Windows Deployment Services]","RetrieveSessions method [Windows Deployment Services]","IWdsTransportContent interface","wds.iwdstransportcontent_retrievesessions","wdstptmgmt/IWdsTransportContent::RetrieveSessions"]
old-location: wds\iwdstransportcontent_retrievesessions.htm
tech.root: wds
ms.assetid: 8901f9c5-931e-40d5-8a5c-d3a814556400
ms.date: 12/05/2018
ms.keywords: IWdsTransportContent interface [Windows Deployment Services],RetrieveSessions method, IWdsTransportContent.RetrieveSessions, IWdsTransportContent::RetrieveSessions, RetrieveSessions, RetrieveSessions method [Windows Deployment Services], RetrieveSessions method [Windows Deployment Services],IWdsTransportContent interface, wds.iwdstransportcontent_retrievesessions, wdstptmgmt/IWdsTransportContent::RetrieveSessions
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
 - IWdsTransportContent::RetrieveSessions
 - wdstptmgmt/IWdsTransportContent::RetrieveSessions
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
 - IWdsTransportContent.RetrieveSessions
---

# IWdsTransportContent::RetrieveSessions


## -description

Retrieves a collection of active transport sessions associated with this content.

## -parameters

### -param ppWdsTransportSessions [out]

A pointer to a collection of objects of the <a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportsession">IWdsTransportSession</a> interface that represent active sessions under this content.

## -returns

Standard HRESULT error values are used: S_OK for success; others for failure.

## -see-also

<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportcontent">IWdsTransportContent</a>