---
UID: NF:wdstptmgmt.IWdsTransportNamespaceManager.CreateNamespace
title: IWdsTransportNamespaceManager::CreateNamespace (wdstptmgmt.h)
description: Creates an object of an IWdsTransportNamespace interface that can be registered on the current WDS transport server.
helpviewer_keywords: ["CreateNamespace","CreateNamespace method [Windows Deployment Services]","CreateNamespace method [Windows Deployment Services]","IWdsTransportNamespaceManager interface","IWdsTransportNamespaceManager interface [Windows Deployment Services]","CreateNamespace method","IWdsTransportNamespaceManager.CreateNamespace","IWdsTransportNamespaceManager::CreateNamespace","wds.iwdstransportnamespacemanager_createnamespace","wdstptmgmt/IWdsTransportNamespaceManager::CreateNamespace"]
old-location: wds\iwdstransportnamespacemanager_createnamespace.htm
tech.root: wds
ms.assetid: fda205d6-f99a-4fec-96bb-0e37e9ca16ce
ms.date: 12/05/2018
ms.keywords: CreateNamespace, CreateNamespace method [Windows Deployment Services], CreateNamespace method [Windows Deployment Services],IWdsTransportNamespaceManager interface, IWdsTransportNamespaceManager interface [Windows Deployment Services],CreateNamespace method, IWdsTransportNamespaceManager.CreateNamespace, IWdsTransportNamespaceManager::CreateNamespace, wds.iwdstransportnamespacemanager_createnamespace, wdstptmgmt/IWdsTransportNamespaceManager::CreateNamespace
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
 - IWdsTransportNamespaceManager::CreateNamespace
 - wdstptmgmt/IWdsTransportNamespaceManager::CreateNamespace
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
 - IWdsTransportNamespaceManager.CreateNamespace
---

# IWdsTransportNamespaceManager::CreateNamespace


## -description

Creates an object of an <a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportnamespace">IWdsTransportNamespace</a> interface that can be registered on the current WDS transport server.

## -parameters

### -param NamespaceType [in]

The type of the new namespace object. This can be one of the namespace types listed by the <a href="/windows/win32/api/wdstptmgmt/ne-wdstptmgmt-wdstransport_namespace_type">WDSTRANSPORT_NAMESPACE_TYPE</a> enumeration.

### -param bszNamespaceName [in]

The name of the new namespace object. If an application attempts to register this namespace with a WDS transport server, WDS confirms that the name is unique.

### -param bszContentProvider [in]

The name of  the content provider to be associated with the new namespace object.

### -param bszConfiguration [in]

The configuration information used by the content provider. The format of this information is defined by the content provider. The value can be an empty string if no parameter is required.

### -param ppWdsTransportNamespace [out]

A pointer to the object of an <a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportnamespace">IWdsTransportNamespace</a> interface created by this method.

## -returns

Standard HRESULT error values are used: S_OK for success; others for failure.

## -see-also

<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportnamespace">IWdsTransportNamespace</a>



<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportnamespacemanager">IWdsTransportNamespaceManager</a>



<a href="/windows/win32/api/wdstptmgmt/ne-wdstptmgmt-wdstransport_namespace_type">WDSTRANSPORT_NAMESPACE_TYPE</a>