---
UID: NF:wcndevice.IWCNConnectNotify.ConnectSucceeded
title: IWCNConnectNotify::ConnectSucceeded
author: windows-sdk-content
description: The IWCNConnectNotify::ConnectSucceeded callback method that indicates a successful IWCNDevice::Connect operation.
old-location: wcn\iwcnconnectnotify_connectsucceeded.htm
tech.root: wcn
ms.assetid: 79c8482a-5cb2-44a7-b324-964bfedd3d2f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ConnectSucceeded, ConnectSucceeded method [Windows Connect Now], ConnectSucceeded method [Windows Connect Now],IWCNConnectNotify interface, IWCNConnectNotify interface [Windows Connect Now],ConnectSucceeded method, IWCNConnectNotify.ConnectSucceeded, IWCNConnectNotify::ConnectSucceeded, wcn.iwcnconnectnotify_connectsucceeded, wcndevice/IWCNConnectNotify::ConnectSucceeded
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
 - IWCNConnectNotify.ConnectSucceeded
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWCNConnectNotify::ConnectSucceeded


## -description


The <b>IWCNConnectNotify::ConnectSucceeded</b> callback method that indicates a successful <a href="https://msdn.microsoft.com/d7c940f2-0862-4b53-bbb9-4ea47fe6d6f6">IWCNDevice::Connect</a> operation.


## -parameters






## -returns



...




## -remarks



Notification of  success does not implicitly indicate that the device is ready, as some devices reboot in order to apply settings provided during the <a href="https://msdn.microsoft.com/d7c940f2-0862-4b53-bbb9-4ea47fe6d6f6">IWCNDevice::Connect</a> operation.

If the <a href="https://msdn.microsoft.com/a092406d-7af4-436d-9755-5a9b87aa6ca9">IWCNDevice</a> interface was used to obtain network settings from a device, then the network profile is immediately ready for use.




## -see-also




<a href="https://msdn.microsoft.com/63ea2b5a-4bec-4050-9a61-962a1faef0a0">IWCNConnectNotify</a>



<a href="https://msdn.microsoft.com/d7c940f2-0862-4b53-bbb9-4ea47fe6d6f6">IWCNDevice::Connect</a>
 

 

