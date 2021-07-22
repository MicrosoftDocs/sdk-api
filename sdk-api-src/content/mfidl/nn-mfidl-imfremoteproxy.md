---
UID: NN:mfidl.IMFRemoteProxy
title: IMFRemoteProxy (mfidl.h)
description: Exposed by objects that act as a proxy for a remote object.
helpviewer_keywords: ["46af5ba7-c362-4cfd-ae6d-b698c6403a65","IMFRemoteProxy","IMFRemoteProxy interface [Media Foundation]","IMFRemoteProxy interface [Media Foundation]","described","mf.imfremoteproxy","mfidl/IMFRemoteProxy"]
old-location: mf\imfremoteproxy.htm
tech.root: mf
ms.assetid: 46af5ba7-c362-4cfd-ae6d-b698c6403a65
ms.date: 12/05/2018
ms.keywords: 46af5ba7-c362-4cfd-ae6d-b698c6403a65, IMFRemoteProxy, IMFRemoteProxy interface [Media Foundation], IMFRemoteProxy interface [Media Foundation],described, mf.imfremoteproxy, mfidl/IMFRemoteProxy
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFRemoteProxy
 - mfidl/IMFRemoteProxy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFRemoteProxy
---

# IMFRemoteProxy interface


## -description

Exposed by objects that act as a proxy for a remote object. To obtain a pointer to this interface, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> with the service identifier MF_REMOTE_PROXY.

## -inheritance

The <b>IMFRemoteProxy</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFRemoteProxy</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/service-interfaces">Service Interfaces</a>
