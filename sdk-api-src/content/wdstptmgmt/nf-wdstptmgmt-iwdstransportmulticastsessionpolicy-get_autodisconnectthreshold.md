---
UID: NF:wdstptmgmt.IWdsTransportMulticastSessionPolicy.get_AutoDisconnectThreshold
title: IWdsTransportMulticastSessionPolicy::get_AutoDisconnectThreshold (wdstptmgmt.h)
author: windows-sdk-content
description: Sets or retrieves the threshold transmission rate, in kilobytes per second, used by the server.
old-location: wds\iwdstransportmulticastsessionpolicy_autodisconnectthreshold.htm
tech.root: wds
ms.assetid: 90f27b8a-97e3-4453-8348-67754c6ab1b9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AutoDisconnectThreshold property [Windows Deployment Services], AutoDisconnectThreshold property [Windows Deployment Services],IWdsTransportMulticastSessionPolicy interface, IWdsTransportMulticastSessionPolicy interface [Windows Deployment Services],AutoDisconnectThreshold property, IWdsTransportMulticastSessionPolicy.AutoDisconnectThreshold, IWdsTransportMulticastSessionPolicy.get_AutoDisconnectThreshold, IWdsTransportMulticastSessionPolicy::AutoDisconnectThreshold, IWdsTransportMulticastSessionPolicy::get_AutoDisconnectThreshold, IWdsTransportMulticastSessionPolicy::put_AutoDisconnectThreshold, get_AutoDisconnectThreshold, wds.iwdstransportmulticastsessionpolicy_autodisconnectthreshold, wdstptmgmt/IWdsTransportMulticastSessionPolicy::AutoDisconnectThreshold, wdstptmgmt/IWdsTransportMulticastSessionPolicy::get_AutoDisconnectThreshold, wdstptmgmt/IWdsTransportMulticastSessionPolicy::put_AutoDisconnectThreshold
ms.topic: method
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
 - IWdsTransportMulticastSessionPolicy.AutoDisconnectThreshold
 - IWdsTransportMulticastSessionPolicy.get_AutoDisconnectThreshold
 - IWdsTransportMulticastSessionPolicy.put_AutoDisconnectThreshold
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWdsTransportMulticastSessionPolicy::get_AutoDisconnectThreshold


## -description


Sets or retrieves  the threshold transmission rate, in kilobytes per second, used by the server.  If the server  has been configured to handle slow clients using the auto-disconnect method, the server disconnects clients that slow the transmission rate below this threshold value.

This property can be used to get or set the value of the threshold transmission rate regardless of which method the server is using to handle  slow clients.

This property is read/write.


## -parameters


## -see-also




<a href="https://msdn.microsoft.com/bb6677d6-7c60-486a-825a-bafec1f3ffed">IWdsTransportMulticastSessionPolicy</a>
 

 

