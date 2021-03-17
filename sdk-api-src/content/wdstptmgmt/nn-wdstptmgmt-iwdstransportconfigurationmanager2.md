---
UID: NN:wdstptmgmt.IWdsTransportConfigurationManager2
title: IWdsTransportConfigurationManager2 (wdstptmgmt.h)
description: This interface inherits from the IWdsTransportConfigurationManager interface and extends it with configuration settings, such as multicast session policy, that are available beginning with Windows Server 2008 R2.
helpviewer_keywords: ["IWdsTransportConfigurationManager2","IWdsTransportConfigurationManager2 interface [Windows Deployment Services]","IWdsTransportConfigurationManager2 interface [Windows Deployment Services]","described","wds.iwdstransportconfigurationmanager2","wdstptmgmt/IWdsTransportConfigurationManager2"]
old-location: wds\iwdstransportconfigurationmanager2.htm
tech.root: wds
ms.assetid: 93e22735-83a4-4037-abea-b72277f8b857
ms.date: 12/05/2018
ms.keywords: IWdsTransportConfigurationManager2, IWdsTransportConfigurationManager2 interface [Windows Deployment Services], IWdsTransportConfigurationManager2 interface [Windows Deployment Services],described, wds.iwdstransportconfigurationmanager2, wdstptmgmt/IWdsTransportConfigurationManager2
req.header: wdstptmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IWdsTransportConfigurationManager2
 - wdstptmgmt/IWdsTransportConfigurationManager2
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
 - IWdsTransportConfigurationManager2
 - IWdsTransportConfigurationManager2.MulticastSessionPolicy
 - IWdsTransportConfigurationManager2.get_MulticastSessionPolicy
---

# IWdsTransportConfigurationManager2 interface


## -description

This interface inherits from the <a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportconfigurationmanager">IWdsTransportConfigurationManager</a> interface and extends it with configuration settings, such as multicast session policy, that are available beginning with Windows Server 2008 R2. 

A client application can obtain an interface pointer to an instance of the <b>IWdsTransportConfigurationManager2</b> interface by first getting an interface pointer to the <a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportconfigurationmanager">IWdsTransportConfigurationManager</a> interface  and then using the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface Method</a>.

## -see-also

<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportconfigurationmanager">IWdsTransportConfigurationManager</a>