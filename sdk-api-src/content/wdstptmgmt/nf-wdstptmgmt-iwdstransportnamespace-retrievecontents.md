---
UID: NF:wdstptmgmt.IWdsTransportNamespace.RetrieveContents
title: IWdsTransportNamespace::RetrieveContents (wdstptmgmt.h)
description: Retrieves a collection of active transport content objects associated with the namespace.
helpviewer_keywords: ["IWdsTransportNamespace interface [Windows Deployment Services]","RetrieveContents method","IWdsTransportNamespace.RetrieveContents","IWdsTransportNamespace::RetrieveContents","RetrieveContents","RetrieveContents method [Windows Deployment Services]","RetrieveContents method [Windows Deployment Services]","IWdsTransportNamespace interface","wds.iwdstransportnamespace_retrievecontents","wdstptmgmt/IWdsTransportNamespace::RetrieveContents"]
old-location: wds\iwdstransportnamespace_retrievecontents.htm
tech.root: wds
ms.assetid: 78afaf1c-f29f-4ab0-8329-d2199ea49c43
ms.date: 12/05/2018
ms.keywords: IWdsTransportNamespace interface [Windows Deployment Services],RetrieveContents method, IWdsTransportNamespace.RetrieveContents, IWdsTransportNamespace::RetrieveContents, RetrieveContents, RetrieveContents method [Windows Deployment Services], RetrieveContents method [Windows Deployment Services],IWdsTransportNamespace interface, wds.iwdstransportnamespace_retrievecontents, wdstptmgmt/IWdsTransportNamespace::RetrieveContents
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
 - IWdsTransportNamespace::RetrieveContents
 - wdstptmgmt/IWdsTransportNamespace::RetrieveContents
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
 - IWdsTransportNamespace.RetrieveContents
---

# IWdsTransportNamespace::RetrieveContents


## -description

Retrieves a collection of active transport content objects associated with the namespace.

## -parameters

### -param ppWdsTransportContents [out]

A pointer to a <a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportcollection">IWdsTransportCollection</a> object that contains a collection of <a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportcontent">IWdsTransportContent</a> objects that represent active sessions under this namespace.

## -returns

Standard HRESULT error values are used: S_OK for success; others for failure.

## -see-also

<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportcollection">IWdsTransportCollection</a>



<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportcontent">IWdsTransportContent</a>



<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportnamespace">IWdsTransportNamespace</a>