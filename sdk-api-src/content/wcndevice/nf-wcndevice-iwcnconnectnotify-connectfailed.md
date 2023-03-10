---
UID: NF:wcndevice.IWCNConnectNotify.ConnectFailed
title: IWCNConnectNotify::ConnectFailed (wcndevice.h)
description: Callback method indicates a IWCNDevice::Connect failure.
helpviewer_keywords: ["ConnectFailed","ConnectFailed method [Windows Connect Now]","ConnectFailed method [Windows Connect Now]","IWCNConnectNotify interface","IWCNConnectNotify interface [Windows Connect Now]","ConnectFailed method","IWCNConnectNotify.ConnectFailed","IWCNConnectNotify::ConnectFailed","wcn.iwcnconnectnotify_connectfailed","wcndevice/IWCNConnectNotify::ConnectFailed"]
old-location: wcn\iwcnconnectnotify_connectfailed.htm
tech.root: wcn
ms.assetid: cdf0394a-f5e6-49cf-bd18-9c3c2b689e50
ms.date: 12/05/2018
ms.keywords: ConnectFailed, ConnectFailed method [Windows Connect Now], ConnectFailed method [Windows Connect Now],IWCNConnectNotify interface, IWCNConnectNotify interface [Windows Connect Now],ConnectFailed method, IWCNConnectNotify.ConnectFailed, IWCNConnectNotify::ConnectFailed, wcn.iwcnconnectnotify_connectfailed, wcndevice/IWCNConnectNotify::ConnectFailed
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
 - IWCNConnectNotify::ConnectFailed
 - wcndevice/IWCNConnectNotify::ConnectFailed
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
 - IWCNConnectNotify.ConnectFailed
---

# IWCNConnectNotify::ConnectFailed


## -description

The <b>IWCNConnectNotify::ConnectFailed</b> callback method  indicates a <a href="/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-connect">IWCNDevice::Connect</a> failure.

## -parameters

### -param hrFailure [in]

An <b>HRESULT</b> that specifies the reason for the connection failure.

## -returns

This method does not return a value.

## -see-also

<a href="/windows/desktop/api/wcndevice/nn-wcndevice-iwcnconnectnotify">IWCNConnectNotify</a>



<a href="/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-connect">IWCNDevice::Connect</a>