---
UID: NN:wdstptmgmt.IWdsTransportServer2
title: IWdsTransportServer2 (wdstptmgmt.h)
description: This interface inherits from the IWdsTransportServer interface and extends it. It is available beginning with Windows Server 2012.
helpviewer_keywords: ["IWdsTransportServer2","IWdsTransportServer2 interface [Windows Deployment Services]","IWdsTransportServer2 interface [Windows Deployment Services]","described","wds.iwdstransportserver2","wdstptmgmt/IWdsTransportServer2"]
old-location: wds\iwdstransportserver2.htm
tech.root: wds
ms.assetid: 27BB5319-74F0-480A-9600-8940491FB7E0
ms.date: 12/05/2018
ms.keywords: IWdsTransportServer2, IWdsTransportServer2 interface [Windows Deployment Services], IWdsTransportServer2 interface [Windows Deployment Services],described, wds.iwdstransportserver2, wdstptmgmt/IWdsTransportServer2
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
 - IWdsTransportServer2
 - wdstptmgmt/IWdsTransportServer2
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
 - IWdsTransportServer2
---

# IWdsTransportServer2 interface


## -description

This interface inherits from the <a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportserver">IWdsTransportServer</a> interface and extends it. It is available  beginning with Windows Server 2012. 

A client application can obtain an interface pointer to an instance of the <b>IWdsTransportServer2</b> interface by first getting an interface pointer to the <a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportserver">IWdsTransportServer</a> interface  and then using the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface Method</a>.

## -see-also

<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportserver">IWdsTransportServer</a>