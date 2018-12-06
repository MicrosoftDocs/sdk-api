---
UID: NN:wdstptmgmt.IWdsTransportMulticastSessionPolicy
title: IWdsTransportMulticastSessionPolicy
author: windows-sdk-content
description: This interface represents the multicast session policy portion of a WDS Transport server’s configuration.
old-location: wds\iwdstransportmulticastsessionpolicy.htm
tech.root: wds
ms.assetid: bb6677d6-7c60-486a-825a-bafec1f3ffed
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWdsTransportMulticastSessionPolicy, IWdsTransportMulticastSessionPolicy interface [Windows Deployment Services], IWdsTransportMulticastSessionPolicy interface [Windows Deployment Services],described, wds.iwdstransportmulticastsessionpolicy, wdstptmgmt/IWdsTransportMulticastSessionPolicy
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wdstptmgmt.dll
api_name:
 - IWdsTransportMulticastSessionPolicy
 - IWdsTransportMulticastSessionPolicy.SlowClientHandling
 - IWdsTransportMulticastSessionPolicy.get_SlowClientHandling
 - IWdsTransportMulticastSessionPolicy.put_SlowClientHandling
 - IWdsTransportMulticastSessionPolicy.AutoDisconnectThreshold
 - IWdsTransportMulticastSessionPolicy.get_AutoDisconnectThreshold
 - IWdsTransportMulticastSessionPolicy.put_AutoDisconnectThreshold
 - IWdsTransportMulticastSessionPolicy.MultistreamStreamCount
 - IWdsTransportMulticastSessionPolicy.get_MultistreamStreamCount
 - IWdsTransportMulticastSessionPolicy.put_MultistreamStreamCount
 - IWdsTransportMulticastSessionPolicy.SlowClientFallback
 - IWdsTransportMulticastSessionPolicy.get_SlowClientFallback
 - IWdsTransportMulticastSessionPolicy.put_SlowClientFallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWdsTransportMulticastSessionPolicy interface


## -description


This interface represents the multicast session policy portion of a WDS Transport server’s configuration. For example, a client can use this interface to configure  the multicast session parameters that specify the method for handling a slow client and the threshold for automatic disconnection.


## -see-also




<a href="https://msdn.microsoft.com/2245d198-056c-467f-aae7-b1bb02f188e2">IWdsTransportCacheable</a>
 

 

