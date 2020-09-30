---
UID: NF:wdstptmgmt.IWdsTransportNamespaceManager.RetrieveNamespaces
title: IWdsTransportNamespaceManager::RetrieveNamespaces (wdstptmgmt.h)
description: Returns a collection of objects of the IWdsTransportNamespace interface that represent namespaces on the server that match specified criteria.
helpviewer_keywords: ["IWdsTransportNamespaceManager interface [Windows Deployment Services]","RetrieveNamespaces method","IWdsTransportNamespaceManager.RetrieveNamespaces","IWdsTransportNamespaceManager::RetrieveNamespaces","RetrieveNamespaces","RetrieveNamespaces method [Windows Deployment Services]","RetrieveNamespaces method [Windows Deployment Services]","IWdsTransportNamespaceManager interface","wds.iwdstransportnamespacemanager_retrievenamespaces","wdstptmgmt/IWdsTransportNamespaceManager::RetrieveNamespaces"]
old-location: wds\iwdstransportnamespacemanager_retrievenamespaces.htm
tech.root: wds
ms.assetid: 3151ab6b-7ceb-4ecc-8480-cb5f9700ca9a
ms.date: 12/05/2018
ms.keywords: IWdsTransportNamespaceManager interface [Windows Deployment Services],RetrieveNamespaces method, IWdsTransportNamespaceManager.RetrieveNamespaces, IWdsTransportNamespaceManager::RetrieveNamespaces, RetrieveNamespaces, RetrieveNamespaces method [Windows Deployment Services], RetrieveNamespaces method [Windows Deployment Services],IWdsTransportNamespaceManager interface, wds.iwdstransportnamespacemanager_retrievenamespaces, wdstptmgmt/IWdsTransportNamespaceManager::RetrieveNamespaces
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
 - IWdsTransportNamespaceManager::RetrieveNamespaces
 - wdstptmgmt/IWdsTransportNamespaceManager::RetrieveNamespaces
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
 - IWdsTransportNamespaceManager.RetrieveNamespaces
---

# IWdsTransportNamespaceManager::RetrieveNamespaces


## -description

Returns a collection of objects of the <a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportnamespace">IWdsTransportNamespace</a> interface that represent namespaces on the server that match specified criteria.

## -parameters

### -param bszContentProvider [in]

The name of the content provider for which namespaces are to be returned. If an empty string is specified, the method returns the namespaces for all content providers.

### -param bszNamespaceName [in]

The name of the namespace for which instances are to be returned. If an empty string is specified, the method returns all namespaces for the selected content providers.

### -param bIncludeTombstones [in]

A value of true specifies that the method should include in the results any namespaces that have been deregistered while still having active sessions on the server. This enables an application to register another namespace with the name.

### -param ppWdsTransportNamespaces [out]

A pointer to the object of an <a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportcollection">IWdsTransportCollection</a> interface.  This represents  a collection  of objects of an <a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportnamespace">IWdsTransportNamespace</a> interface that match the specified criteria.

## -returns

Standard HRESULT error values are used: S_OK for success; others for failure.

## -see-also

<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportcollection">IWdsTransportCollection</a>



<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportnamespace">IWdsTransportNamespace</a>



<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportnamespacemanager">IWdsTransportNamespaceManager</a>