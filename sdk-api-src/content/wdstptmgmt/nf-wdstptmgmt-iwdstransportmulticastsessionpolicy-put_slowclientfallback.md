---
UID: NF:wdstptmgmt.IWdsTransportMulticastSessionPolicy.put_SlowClientFallback
title: IWdsTransportMulticastSessionPolicy::put_SlowClientFallback (wdstptmgmt.h)
description: Receives a value that indicates the fallback policy requested by the server when automatically disconnecting slow clients from a multicast transmission. (Put)
helpviewer_keywords: ["IWdsTransportMulticastSessionPolicy interface [Windows Deployment Services]","SlowClientFallback property","IWdsTransportMulticastSessionPolicy.SlowClientFallback","IWdsTransportMulticastSessionPolicy.put_SlowClientFallback","IWdsTransportMulticastSessionPolicy::SlowClientFallback","IWdsTransportMulticastSessionPolicy::get_SlowClientFallback","IWdsTransportMulticastSessionPolicy::put_SlowClientFallback","SlowClientFallback property [Windows Deployment Services]","SlowClientFallback property [Windows Deployment Services]","IWdsTransportMulticastSessionPolicy interface","put_SlowClientFallback","wds.iwdstransportmulticastsessionpolicy_slowclientfallback","wdstptmgmt/IWdsTransportMulticastSessionPolicy::SlowClientFallback","wdstptmgmt/IWdsTransportMulticastSessionPolicy::get_SlowClientFallback","wdstptmgmt/IWdsTransportMulticastSessionPolicy::put_SlowClientFallback"]
old-location: wds\iwdstransportmulticastsessionpolicy_slowclientfallback.htm
tech.root: wds
ms.assetid: cce0ba98-382a-45d5-8381-06864061c529
ms.date: 12/05/2018
ms.keywords: IWdsTransportMulticastSessionPolicy interface [Windows Deployment Services],SlowClientFallback property, IWdsTransportMulticastSessionPolicy.SlowClientFallback, IWdsTransportMulticastSessionPolicy.put_SlowClientFallback, IWdsTransportMulticastSessionPolicy::SlowClientFallback, IWdsTransportMulticastSessionPolicy::get_SlowClientFallback, IWdsTransportMulticastSessionPolicy::put_SlowClientFallback, SlowClientFallback property [Windows Deployment Services], SlowClientFallback property [Windows Deployment Services],IWdsTransportMulticastSessionPolicy interface, put_SlowClientFallback, wds.iwdstransportmulticastsessionpolicy_slowclientfallback, wdstptmgmt/IWdsTransportMulticastSessionPolicy::SlowClientFallback, wdstptmgmt/IWdsTransportMulticastSessionPolicy::get_SlowClientFallback, wdstptmgmt/IWdsTransportMulticastSessionPolicy::put_SlowClientFallback
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
 - IWdsTransportMulticastSessionPolicy::put_SlowClientFallback
 - wdstptmgmt/IWdsTransportMulticastSessionPolicy::put_SlowClientFallback
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
 - IWdsTransportMulticastSessionPolicy.SlowClientFallback
 - IWdsTransportMulticastSessionPolicy.get_SlowClientFallback
 - IWdsTransportMulticastSessionPolicy.put_SlowClientFallback
---

# IWdsTransportMulticastSessionPolicy::put_SlowClientFallback


## -description

Receives  a value that indicates the fallback policy requested by the server when automatically disconnecting slow clients from a multicast transmission. A value of <b>VARIANT_FALSE</b> requests that the client disconnect from the server and discontinue any further attempts to get the content from this server. A value of <b>VARIANT_TRUE</b> requests that the client use any alternative method available to the client to get the content, for example  unicasting. 

This property can be used to get or set the fallback policy regardless of which method the server is using to handle  slow clients.

This policy is only used when the server is automatically disconnecting a slow client from a multicast transmission. An administrator  manually disconnecting a client, can specify the fallback method.

This property is read/write.

## -parameters

## -see-also

<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportmulticastsessionpolicy">IWdsTransportMulticastSessionPolicy</a>
