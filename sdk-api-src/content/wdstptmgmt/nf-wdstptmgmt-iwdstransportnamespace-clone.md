---
UID: NF:wdstptmgmt.IWdsTransportNamespace.Clone
title: IWdsTransportNamespace::Clone (wdstptmgmt.h)
description: Copies the information from this namespace object into a new, unregistered namespace object in memory.
helpviewer_keywords: ["Clone","Clone method [Windows Deployment Services]","Clone method [Windows Deployment Services]","IWdsTransportNamespace interface","IWdsTransportNamespace interface [Windows Deployment Services]","Clone method","IWdsTransportNamespace.Clone","IWdsTransportNamespace::Clone","wds.iwdstransportnamespace_clone","wdstptmgmt/IWdsTransportNamespace::Clone"]
old-location: wds\iwdstransportnamespace_clone.htm
tech.root: wds
ms.assetid: bc7eb27e-8bbb-414a-bfc2-25cc762b451d
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Windows Deployment Services], Clone method [Windows Deployment Services],IWdsTransportNamespace interface, IWdsTransportNamespace interface [Windows Deployment Services],Clone method, IWdsTransportNamespace.Clone, IWdsTransportNamespace::Clone, wds.iwdstransportnamespace_clone, wdstptmgmt/IWdsTransportNamespace::Clone
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
 - IWdsTransportNamespace::Clone
 - wdstptmgmt/IWdsTransportNamespace::Clone
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
 - IWdsTransportNamespace.Clone
---

# IWdsTransportNamespace::Clone


## -description

Copies the information from this namespace object into a new, unregistered namespace object in memory.

## -parameters

### -param ppWdsTransportNamespaceClone [out]

An interface pointer to a new, unregistered copy of this namespace.

## -returns

Standard HRESULT error values are used: S_OK for success; others for failure.

## -see-also

<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportnamespace">IWdsTransportNamespace</a>