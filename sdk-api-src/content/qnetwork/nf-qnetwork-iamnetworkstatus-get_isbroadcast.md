---
UID: NF:qnetwork.IAMNetworkStatus.get_IsBroadcast
title: IAMNetworkStatus::get_IsBroadcast
author: windows-sdk-content
description: The get_IsBroadcast method retrieves a value indicating whether the current stream is a broadcast stream.
old-location: dshow\iamnetworkstatus_get_isbroadcast.htm
old-project: DirectShow
ms.assetid: 578fe82b-0c87-47ea-9600-91d68f4c733f
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IAMNetworkStatus interface [DirectShow],get_IsBroadcast method, IAMNetworkStatus.get_IsBroadcast, IAMNetworkStatus::get_IsBroadcast, IAMNetworkStatusget_IsBroadcast, dshow.iamnetworkstatus_get_isbroadcast, get_IsBroadcast, get_IsBroadcast method [DirectShow], get_IsBroadcast method [DirectShow],IAMNetworkStatus interface, qnetwork/IAMNetworkStatus::get_IsBroadcast
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: qnetwork.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AMExtendedSeekingCapabilities
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMNetworkStatus.get_IsBroadcast
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IAMNetworkStatus::get_IsBroadcast


## -description



The <code>get_IsBroadcast</code> method retrieves a value indicating whether the current stream is a broadcast stream.




## -parameters




### -param pIsBroadcast

Pointer to a variable that receives a Boolean value.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



A broadcast stream can be unicast or multicast. In a broadcast connection, the client is passive and does not control when the stream starts or stops. In an on-demand connection, the client is active and controls when the stream is started and stopped.




## -see-also




<a href="https://msdn.microsoft.com/51d56b76-f9fc-44e1-88f0-d35d861a4697">IAMNetworkStatus Interface</a>
 

 

