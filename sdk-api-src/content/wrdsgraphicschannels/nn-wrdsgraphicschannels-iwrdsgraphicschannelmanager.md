---
UID: NN:wrdsgraphicschannels.IWRdsGraphicsChannelManager
title: IWRdsGraphicsChannelManager (wrdsgraphicschannels.h)
description: This interface is used by the RemoteFX graphics services API to create the graphics virtual channels necessary for remoting graphics data.
helpviewer_keywords: ["IWRdsGraphicsChannelManager","IWRdsGraphicsChannelManager interface [Remote Desktop Services]","IWRdsGraphicsChannelManager interface [Remote Desktop Services]","described","termserv.iwrdsgraphicschannelmanager","wrdsgraphicschannels/IWRdsGraphicsChannelManager"]
old-location: termserv\iwrdsgraphicschannelmanager.htm
tech.root: TermServ
ms.assetid: 629589cb-9879-491d-a224-6ae2ce8b0ea3
ms.date: 12/05/2018
ms.keywords: IWRdsGraphicsChannelManager, IWRdsGraphicsChannelManager interface [Remote Desktop Services], IWRdsGraphicsChannelManager interface [Remote Desktop Services],described, termserv.iwrdsgraphicschannelmanager, wrdsgraphicschannels/IWRdsGraphicsChannelManager
req.header: wrdsgraphicschannels.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wrdsgraphicschannels.idl
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
 - IWRdsGraphicsChannelManager
 - wrdsgraphicschannels/IWRdsGraphicsChannelManager
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wrdsgraphicschannels.h
api_name:
 - IWRdsGraphicsChannelManager
---

# IWRdsGraphicsChannelManager interface


## -description

This interface is used by the RemoteFX graphics services API to create the graphics virtual channels necessary for remoting graphics data. The channel implementer provides a pointer to this interface in the <a href="https://github.com/MicrosoftDocs/sdk-api/blob/docs/sdk-api-src/content/wtsprotocol/nf-wtsprotocol-iwrdsremotefxgraphicsconnection-getvirtualchanneltransport.md">IWRdsRemoteFXGraphicsConnection::GetVirtualChannelTransport</a> method.

## -inheritance

The <b>IWRdsGraphicsChannelManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWRdsGraphicsChannelManager</b> also has these types of members:

## -see-also

<a href="https://github.com/MicrosoftDocs/sdk-api/blob/docs/sdk-api-src/content/wtsprotocol/nf-wtsprotocol-iwrdsremotefxgraphicsconnection-getvirtualchanneltransport.md">IWRdsRemoteFXGraphicsConnection::GetVirtualChannelTransport</a>
