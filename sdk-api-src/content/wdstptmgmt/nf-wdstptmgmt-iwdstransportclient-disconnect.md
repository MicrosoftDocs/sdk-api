---
UID: NF:wdstptmgmt.IWdsTransportClient.Disconnect
title: IWdsTransportClient::Disconnect (wdstptmgmt.h)
description: Disconnects the WDS client from the session and specifies what action the client should take upon disconnection.
helpviewer_keywords: ["Disconnect","Disconnect method [Windows Deployment Services]","Disconnect method [Windows Deployment Services]","IWdsTransportClient interface","IWdsTransportClient interface [Windows Deployment Services]","Disconnect method","IWdsTransportClient.Disconnect","IWdsTransportClient::Disconnect","wds.iwdstransportclient_disconnect","wdstptmgmt/IWdsTransportClient::Disconnect"]
old-location: wds\iwdstransportclient_disconnect.htm
tech.root: wds
ms.assetid: faf3ab18-2629-402f-96ad-41337c165fba
ms.date: 12/05/2018
ms.keywords: Disconnect, Disconnect method [Windows Deployment Services], Disconnect method [Windows Deployment Services],IWdsTransportClient interface, IWdsTransportClient interface [Windows Deployment Services],Disconnect method, IWdsTransportClient.Disconnect, IWdsTransportClient::Disconnect, wds.iwdstransportclient_disconnect, wdstptmgmt/IWdsTransportClient::Disconnect
req.header: wdstptmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IWdsTransportClient::Disconnect
 - wdstptmgmt/IWdsTransportClient::Disconnect
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
 - IWdsTransportClient.Disconnect
---

# IWdsTransportClient::Disconnect


## -description

Disconnects the WDS client from the session and specifies what action the client should take upon disconnection.

## -parameters

### -param DisconnectionType [in]

A value of the <a href="/windows/win32/api/wdstptmgmt/ne-wdstptmgmt-wdstransport_disconnect_type">WDSTRANSPORT_DISCONNECT_TYPE</a> enumeration that specifies what action the WDS client should take when disconnected.

## -returns

Standard HRESULT error values are used: S_OK for success; others for failure.

## -see-also

<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportclient">IWdsTransportClient</a>



<a href="/windows/win32/api/wdstptmgmt/ne-wdstptmgmt-wdstransport_disconnect_type">WDSTRANSPORT_DISCONNECT_TYPE</a>