---
UID: NF:wdstptmgmt.IWdsTransportNamespaceManager.RetrieveNamespace
title: IWdsTransportNamespaceManager::RetrieveNamespace (wdstptmgmt.h)
description: Retrieves, by name, an object of an IWdsTransportNamespace interface. The name should be registered with the namespace on the WDS transport server.
helpviewer_keywords: ["IWdsTransportNamespaceManager interface [Windows Deployment Services]","RetrieveNamespace method","IWdsTransportNamespaceManager.RetrieveNamespace","IWdsTransportNamespaceManager::RetrieveNamespace","RetrieveNamespace","RetrieveNamespace method [Windows Deployment Services]","RetrieveNamespace method [Windows Deployment Services]","IWdsTransportNamespaceManager interface","wds.iwdstransportnamespacemanager_retrievenamespace","wdstptmgmt/IWdsTransportNamespaceManager::RetrieveNamespace"]
old-location: wds\iwdstransportnamespacemanager_retrievenamespace.htm
tech.root: wds
ms.assetid: 8afe8d0c-4c6b-45a6-a330-b2cee59ca1ad
ms.date: 12/05/2018
ms.keywords: IWdsTransportNamespaceManager interface [Windows Deployment Services],RetrieveNamespace method, IWdsTransportNamespaceManager.RetrieveNamespace, IWdsTransportNamespaceManager::RetrieveNamespace, RetrieveNamespace, RetrieveNamespace method [Windows Deployment Services], RetrieveNamespace method [Windows Deployment Services],IWdsTransportNamespaceManager interface, wds.iwdstransportnamespacemanager_retrievenamespace, wdstptmgmt/IWdsTransportNamespaceManager::RetrieveNamespace
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
 - IWdsTransportNamespaceManager::RetrieveNamespace
 - wdstptmgmt/IWdsTransportNamespaceManager::RetrieveNamespace
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
 - IWdsTransportNamespaceManager.RetrieveNamespace
---

# IWdsTransportNamespaceManager::RetrieveNamespace


## -description

Retrieves,  by name, an object of an <a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportnamespace">IWdsTransportNamespace</a> interface. The name  should be registered with the namespace on the WDS transport server.

## -parameters

### -param bszNamespaceName [in]

The name of the namespace for which an object is being returned.  The namespace should be registered with the WDS transport server.

### -param ppWdsTransportNamespace [out]

A pointer to the object of an <a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportnamespace">IWdsTransportNamespace</a> interface that matches the specified name.

## -returns

Standard HRESULT error values are used: S_OK for success; others for failure.

## -see-also

<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportnamespace">IWdsTransportNamespace</a>



<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportnamespacemanager">IWdsTransportNamespaceManager</a>