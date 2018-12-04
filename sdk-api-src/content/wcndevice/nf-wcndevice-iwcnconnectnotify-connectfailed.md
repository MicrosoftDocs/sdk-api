---
UID: NF:wcndevice.IWCNConnectNotify.ConnectFailed
title: IWCNConnectNotify::ConnectFailed
author: windows-sdk-content
description: Callback method indicates a IWCNDevice::Connect failure.
old-location: wcn\iwcnconnectnotify_connectfailed.htm
tech.root: wcn
ms.assetid: cdf0394a-f5e6-49cf-bd18-9c3c2b689e50
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ConnectFailed, ConnectFailed method [Windows Connect Now], ConnectFailed method [Windows Connect Now],IWCNConnectNotify interface, IWCNConnectNotify interface [Windows Connect Now],ConnectFailed method, IWCNConnectNotify.ConnectFailed, IWCNConnectNotify::ConnectFailed, wcn.iwcnconnectnotify_connectfailed, wcndevice/IWCNConnectNotify::ConnectFailed
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wcndevice.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcnDevice.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WcnDevice.h
api_name:
 - IWCNConnectNotify.ConnectFailed
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWCNConnectNotify::ConnectFailed


## -description


The <b>IWCNConnectNotify::ConnectFailed</b> callback method  indicates a <a href="https://msdn.microsoft.com/d7c940f2-0862-4b53-bbb9-4ea47fe6d6f6">IWCNDevice::Connect</a> failure.


## -parameters




### -param hrFailure [in]

An <b>HRESULT</b> that specifies the reason for the connection failure.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/63ea2b5a-4bec-4050-9a61-962a1faef0a0">IWCNConnectNotify</a>



<a href="https://msdn.microsoft.com/d7c940f2-0862-4b53-bbb9-4ea47fe6d6f6">IWCNDevice::Connect</a>
 

 

