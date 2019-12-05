---
UID: NF:wcndevice.IWCNConnectNotify.ConnectSucceeded
title: IWCNConnectNotify::ConnectSucceeded (wcndevice.h)
description: The IWCNConnectNotify::ConnectSucceeded callback method that indicates a successful IWCNDevice::Connect operation.
old-location: wcn\iwcnconnectnotify_connectsucceeded.htm
tech.root: wcn
ms.assetid: 79c8482a-5cb2-44a7-b324-964bfedd3d2f
ms.date: 12/05/2018
ms.keywords: ConnectSucceeded, ConnectSucceeded method [Windows Connect Now], ConnectSucceeded method [Windows Connect Now],IWCNConnectNotify interface, IWCNConnectNotify interface [Windows Connect Now],ConnectSucceeded method, IWCNConnectNotify.ConnectSucceeded, IWCNConnectNotify::ConnectSucceeded, wcn.iwcnconnectnotify_connectsucceeded, wcndevice/IWCNConnectNotify::ConnectSucceeded
ms.topic: method
f1_keywords:
- wcndevice/IWCNConnectNotify.ConnectSucceeded
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWCNConnectNotify::ConnectSucceeded


## -description


The <b>IWCNConnectNotify::ConnectSucceeded</b> callback method that indicates a successful <a href="https://docs.microsoft.com/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-connect">IWCNDevice::Connect</a> operation.


## -parameters






## -returns



...




## -remarks



Notification of  success does not implicitly indicate that the device is ready, as some devices reboot in order to apply settings provided during the <a href="https://docs.microsoft.com/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-connect">IWCNDevice::Connect</a> operation.

If the <a href="https://docs.microsoft.com/windows/desktop/api/wcndevice/nn-wcndevice-iwcndevice">IWCNDevice</a> interface was used to obtain network settings from a device, then the network profile is immediately ready for use.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wcndevice/nn-wcndevice-iwcnconnectnotify">IWCNConnectNotify</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-connect">IWCNDevice::Connect</a>
 

 

