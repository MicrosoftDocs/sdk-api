---
UID: NN:wdstptmgmt.IWdsTransportSetupManager2
title: IWdsTransportSetupManager2 (wdstptmgmt.h)
description: This interface inherits from the IWdsTransportSetupManager interface and extends it. It is available beginning with Windows Server 2012.
helpviewer_keywords: ["IWdsTransportSetupManager2","IWdsTransportSetupManager2 interface [Windows Deployment Services]","IWdsTransportSetupManager2 interface [Windows Deployment Services]","described","wds.iwdstransportsetupmanager2","wdstptmgmt/IWdsTransportSetupManager2"]
old-location: wds\iwdstransportsetupmanager2.htm
tech.root: wds
ms.assetid: C16D037D-8E6C-4789-8947-D3BAC73D86FF
ms.date: 12/05/2018
ms.keywords: IWdsTransportSetupManager2, IWdsTransportSetupManager2 interface [Windows Deployment Services], IWdsTransportSetupManager2 interface [Windows Deployment Services],described, wds.iwdstransportsetupmanager2, wdstptmgmt/IWdsTransportSetupManager2
req.header: wdstptmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IWdsTransportSetupManager2
 - wdstptmgmt/IWdsTransportSetupManager2
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
 - IWdsTransportSetupManager2
---

# IWdsTransportSetupManager2 interface


## -description

This interface inherits from the <a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportsetupmanager">IWdsTransportSetupManager</a> interface and extends it. It is available beginning with Windows Server 2012. 

A client application can obtain an interface pointer to an instance of the <b>IWdsTransportSetupManager2</b> interface by first getting an interface pointer to the <a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportsetupmanager">IWdsTransportSetupManager</a> interface  and then using the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface Method</a>.

## -see-also

<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportcollection">IWdsTransportCollection</a>



<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportsetupmanager">IWdsTransportSetupManager</a>