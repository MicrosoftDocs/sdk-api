---
UID: NF:wcndevice.IWCNConnectNotify.ConnectSucceeded
title: IWCNConnectNotify::ConnectSucceeded (wcndevice.h)
description: The IWCNConnectNotify::ConnectSucceeded callback method that indicates a successful IWCNDevice::Connect operation.
helpviewer_keywords: ["ConnectSucceeded","ConnectSucceeded method [Windows Connect Now]","ConnectSucceeded method [Windows Connect Now]","IWCNConnectNotify interface","IWCNConnectNotify interface [Windows Connect Now]","ConnectSucceeded method","IWCNConnectNotify.ConnectSucceeded","IWCNConnectNotify::ConnectSucceeded","wcn.iwcnconnectnotify_connectsucceeded","wcndevice/IWCNConnectNotify::ConnectSucceeded"]
old-location: wcn\iwcnconnectnotify_connectsucceeded.htm
tech.root: wcn
ms.assetid: 79c8482a-5cb2-44a7-b324-964bfedd3d2f
ms.date: 12/05/2018
ms.keywords: ConnectSucceeded, ConnectSucceeded method [Windows Connect Now], ConnectSucceeded method [Windows Connect Now],IWCNConnectNotify interface, IWCNConnectNotify interface [Windows Connect Now],ConnectSucceeded method, IWCNConnectNotify.ConnectSucceeded, IWCNConnectNotify::ConnectSucceeded, wcn.iwcnconnectnotify_connectsucceeded, wcndevice/IWCNConnectNotify::ConnectSucceeded
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWCNConnectNotify::ConnectSucceeded
 - wcndevice/IWCNConnectNotify::ConnectSucceeded
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WcnDevice.h
api_name:
 - IWCNConnectNotify.ConnectSucceeded
---

# IWCNConnectNotify::ConnectSucceeded


## -description

The <b>IWCNConnectNotify::ConnectSucceeded</b> callback method that indicates a successful <a href="/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-connect">IWCNDevice::Connect</a> operation.



## -returns

...

## -remarks

Notification of  success does not implicitly indicate that the device is ready, as some devices reboot in order to apply settings provided during the <a href="/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-connect">IWCNDevice::Connect</a> operation.

If the <a href="/windows/desktop/api/wcndevice/nn-wcndevice-iwcndevice">IWCNDevice</a> interface was used to obtain network settings from a device, then the network profile is immediately ready for use.

## -see-also

<a href="/windows/desktop/api/wcndevice/nn-wcndevice-iwcnconnectnotify">IWCNConnectNotify</a>



<a href="/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-connect">IWCNDevice::Connect</a>
