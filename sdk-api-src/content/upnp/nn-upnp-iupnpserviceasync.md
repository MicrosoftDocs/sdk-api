---
UID: NN:upnp.IUPnPServiceAsync
title: IUPnPServiceAsync (upnp.h)
description: Use this interface to asynchronously query state variables and invoke actions on an instance of a service .
helpviewer_keywords: ["IUPnPServiceAsync","IUPnPServiceAsync interface [UPnP APIs]","IUPnPServiceAsync interface [UPnP APIs]","described","upnp.iupnpserviceasync","upnp/IUPnPServiceAsync"]
old-location: upnp\iupnpserviceasync.htm
tech.root: upnp
ms.assetid: B77025D6-26C7-46C9-84FE-69685C61735D
ms.date: 12/05/2018
ms.keywords: IUPnPServiceAsync, IUPnPServiceAsync interface [UPnP APIs], IUPnPServiceAsync interface [UPnP APIs],described, upnp.iupnpserviceasync, upnp/IUPnPServiceAsync
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Upnp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUPnPServiceAsync
 - upnp/IUPnPServiceAsync
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPServiceAsync
---

# IUPnPServiceAsync interface


## -description

Use this interface to asynchronously query state variables and invoke actions on an instance of a service .

This interface can be obtained through a <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> off the <a href="/windows/desktop/api/upnp/nn-upnp-iupnpservice">IUPnPService</a> object.

## -inheritance

The <b>IUPnPServiceAsync</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUPnPServiceAsync</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpasyncresult">IUPnPAsyncResult</a>
