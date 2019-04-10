---
UID: NF:tsvirtualchannels.IWTSListenerCallback.OnNewChannelConnection
title: IWTSListenerCallback::OnNewChannelConnection (tsvirtualchannels.h)
author: windows-sdk-content
description: Allows the Remote Desktop Connection (RDC) client plug-in to accept or deny a connection request for an incoming connection.
old-location: termserv\iwtslistenercallback_onnewchannelconnection.htm
tech.root: TermServ
ms.assetid: 1fa2b063-3a41-4f56-8cc1-8a829e530fb2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWTSListenerCallback interface [Remote Desktop Services],OnNewChannelConnection method, IWTSListenerCallback.OnNewChannelConnection, IWTSListenerCallback::OnNewChannelConnection, OnNewChannelConnection, OnNewChannelConnection method [Remote Desktop Services], OnNewChannelConnection method [Remote Desktop Services],IWTSListenerCallback interface, termserv.iwtslistenercallback_onnewchannelconnection, tsvirtualchannels/IWTSListenerCallback::OnNewChannelConnection
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - TsVirtualChannels.h
api_name:
 - IWTSListenerCallback.OnNewChannelConnection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWTSListenerCallback::OnNewChannelConnection


## -description


Allows the Remote Desktop Connection (RDC) client plug-in to accept or deny a connection request for an 
    incoming connection.


## -parameters




### -param pChannel [in]

An <a href="https://msdn.microsoft.com/d90c6f80-ed4c-4b99-af85-d2c5816ade85">IWTSVirtualChannel</a> object that 
      represents the incoming connection. This object will only be connected if the connection is accepted by this 
      method.


### -param data [in]

This parameter is not implemented and is reserved for future use.


### -param pbAccept [out]

Indicates whether the connection should be accepted. Receives <b>TRUE</b> if the 
      connection should be accepted or <b>FALSE</b> otherwise.


### -param ppCallback [out]

Receives an 
      <a href="https://msdn.microsoft.com/d90c6f80-ed4c-4b99-af85-d2c5816ade85">IWTSVirtualChannelCallback</a> object that 
      receives notifications for the connection. This object is created by the plug-in.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ecc673ec-1bea-4e7c-b1b5-a2342445f6cf">DVC Client Plug-in Example</a>



<a href="https://msdn.microsoft.com/b5f1d74d-31e6-4447-82ab-6dd3ad9957fd">IWTSListenerCallback</a>



<a href="https://msdn.microsoft.com/d90c6f80-ed4c-4b99-af85-d2c5816ade85">IWTSVirtualChannel</a>



<a href="https://msdn.microsoft.com/d90c6f80-ed4c-4b99-af85-d2c5816ade85">IWTSVirtualChannelCallback</a>
 

 

