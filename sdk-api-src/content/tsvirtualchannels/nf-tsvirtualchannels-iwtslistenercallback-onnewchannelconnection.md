---
UID: NF:tsvirtualchannels.IWTSListenerCallback.OnNewChannelConnection
title: IWTSListenerCallback::OnNewChannelConnection (tsvirtualchannels.h)
description: Allows the Remote Desktop Connection (RDC) client plug-in to accept or deny a connection request for an incoming connection.
helpviewer_keywords: ["IWTSListenerCallback interface [Remote Desktop Services]","OnNewChannelConnection method","IWTSListenerCallback.OnNewChannelConnection","IWTSListenerCallback::OnNewChannelConnection","OnNewChannelConnection","OnNewChannelConnection method [Remote Desktop Services]","OnNewChannelConnection method [Remote Desktop Services]","IWTSListenerCallback interface","termserv.iwtslistenercallback_onnewchannelconnection","tsvirtualchannels/IWTSListenerCallback::OnNewChannelConnection"]
old-location: termserv\iwtslistenercallback_onnewchannelconnection.htm
tech.root: TermServ
ms.assetid: 1fa2b063-3a41-4f56-8cc1-8a829e530fb2
ms.date: 12/05/2018
ms.keywords: IWTSListenerCallback interface [Remote Desktop Services],OnNewChannelConnection method, IWTSListenerCallback.OnNewChannelConnection, IWTSListenerCallback::OnNewChannelConnection, OnNewChannelConnection, OnNewChannelConnection method [Remote Desktop Services], OnNewChannelConnection method [Remote Desktop Services],IWTSListenerCallback interface, termserv.iwtslistenercallback_onnewchannelconnection, tsvirtualchannels/IWTSListenerCallback::OnNewChannelConnection
req.header: tsvirtualchannels.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: TsVirtualChannels.idl
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
 - IWTSListenerCallback::OnNewChannelConnection
 - tsvirtualchannels/IWTSListenerCallback::OnNewChannelConnection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - TsVirtualChannels.h
api_name:
 - IWTSListenerCallback.OnNewChannelConnection
---

# IWTSListenerCallback::OnNewChannelConnection


## -description

Allows the Remote Desktop Connection (RDC) client plug-in to accept or deny a connection request for an 
    incoming connection.

## -parameters

### -param pChannel [in]

An <a href="/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback">IWTSVirtualChannel</a> object that 
      represents the incoming connection. This object will only be connected if the connection is accepted by this 
      method.

### -param data [in]

This parameter is not implemented and is reserved for future use.

### -param pbAccept [out]

Indicates whether the connection should be accepted. Receives <b>TRUE</b> if the 
      connection should be accepted or <b>FALSE</b> otherwise.

### -param ppCallback [out]

Receives an 
      <a href="/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback">IWTSVirtualChannelCallback</a> object that 
      receives notifications for the connection. This object is created by the plug-in.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/TermServ/dvc-client-plug-in-example">DVC Client Plug-in Example</a>



<a href="/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtslistenercallback">IWTSListenerCallback</a>



<a href="/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback">IWTSVirtualChannel</a>



<a href="/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback">IWTSVirtualChannelCallback</a>