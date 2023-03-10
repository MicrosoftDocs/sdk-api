---
UID: NF:wdstptmgmt.IWdsTransportNamespace.Refresh
title: IWdsTransportNamespace::Refresh (wdstptmgmt.h)
description: Resets the property values of the namespace with values from the server.
helpviewer_keywords: ["IWdsTransportNamespace interface [Windows Deployment Services]","Refresh method","IWdsTransportNamespace.Refresh","IWdsTransportNamespace::Refresh","Refresh","Refresh method [Windows Deployment Services]","Refresh method [Windows Deployment Services]","IWdsTransportNamespace interface","wds.iwdstransportnamespace_refresh","wdstptmgmt/IWdsTransportNamespace::Refresh"]
old-location: wds\iwdstransportnamespace_refresh.htm
tech.root: wds
ms.assetid: 9d5742e0-4197-4a15-82c6-5623940c0c7f
ms.date: 12/05/2018
ms.keywords: IWdsTransportNamespace interface [Windows Deployment Services],Refresh method, IWdsTransportNamespace.Refresh, IWdsTransportNamespace::Refresh, Refresh, Refresh method [Windows Deployment Services], Refresh method [Windows Deployment Services],IWdsTransportNamespace interface, wds.iwdstransportnamespace_refresh, wdstptmgmt/IWdsTransportNamespace::Refresh
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
 - IWdsTransportNamespace::Refresh
 - wdstptmgmt/IWdsTransportNamespace::Refresh
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
 - IWdsTransportNamespace.Refresh
---

# IWdsTransportNamespace::Refresh


## -description

Resets the property values of the namespace with values from the server.



## -returns

Standard HRESULT error values are used: S_OK for success; others for failure.

## -remarks

The method fails if the namespace object has never been registered on the server.

## -see-also

<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportnamespace">IWdsTransportNamespace</a>
