---
UID: NN:wdstptmgmt.IWdsTransportServicePolicy2
title: IWdsTransportServicePolicy2 (wdstptmgmt.h)
description: This interface inherits from the IWdsTransportServicePolicy interface and extends it beginning with Windows Server 2012.
helpviewer_keywords: ["IWdsTransportServicePolicy2","IWdsTransportServicePolicy2 interface [Windows Deployment Services]","IWdsTransportServicePolicy2 interface [Windows Deployment Services]","described","wds.iwdstransportservicepolicy2","wdstptmgmt/IWdsTransportServicePolicy2"]
old-location: wds\iwdstransportservicepolicy2.htm
tech.root: wds
ms.assetid: F03FC0C8-D589-4C3C-A6C1-AD631839ED26
ms.date: 12/05/2018
ms.keywords: IWdsTransportServicePolicy2, IWdsTransportServicePolicy2 interface [Windows Deployment Services], IWdsTransportServicePolicy2 interface [Windows Deployment Services],described, wds.iwdstransportservicepolicy2, wdstptmgmt/IWdsTransportServicePolicy2
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
 - IWdsTransportServicePolicy2
 - wdstptmgmt/IWdsTransportServicePolicy2
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
 - IWdsTransportServicePolicy2
---

# IWdsTransportServicePolicy2 interface


## -description

This interface inherits from the <a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportservicepolicy">IWdsTransportServicePolicy</a> interface and extends it beginning with Windows Server 2012. 

A client application can obtain an interface pointer to an instance of the <b>IWdsTransportServicePolicy2</b> interface by first getting an interface pointer to the <a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportservicepolicy">IWdsTransportServicePolicy</a> interface  and then using the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface Method</a>.

## -see-also

<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportservicepolicy">IWdsTransportServicePolicy</a>



<a href="/windows/win32/api/wdstptmgmt/ne-wdstptmgmt-wdstransport_tftp_capability">WDSTRANSPORT_TFTP_CAPABILITY</a>