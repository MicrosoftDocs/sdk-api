---
UID: NN:wrdsgraphicschannels.IWRdsGraphicsChannelEvents
title: IWRdsGraphicsChannelEvents (wrdsgraphicschannels.h)
description: This interface receives notifications that relate to a graphics virtual channel.
helpviewer_keywords: ["IWRdsGraphicsChannelEvents","IWRdsGraphicsChannelEvents interface [Remote Desktop Services]","IWRdsGraphicsChannelEvents interface [Remote Desktop Services]","described","termserv.iwrdsgraphicschannelevents","wrdsgraphicschannels/IWRdsGraphicsChannelEvents"]
old-location: termserv\iwrdsgraphicschannelevents.htm
tech.root: TermServ
ms.assetid: 59802a2d-bdb0-4792-b667-5095d4a02b06
ms.date: 12/05/2018
ms.keywords: IWRdsGraphicsChannelEvents, IWRdsGraphicsChannelEvents interface [Remote Desktop Services], IWRdsGraphicsChannelEvents interface [Remote Desktop Services],described, termserv.iwrdsgraphicschannelevents, wrdsgraphicschannels/IWRdsGraphicsChannelEvents
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
 - IWRdsGraphicsChannelEvents
 - wrdsgraphicschannels/IWRdsGraphicsChannelEvents
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
 - IWRdsGraphicsChannelEvents
---

# IWRdsGraphicsChannelEvents interface


## -description

This interface receives notifications that relate to a graphics virtual channel. This interface is implemented by the RemoteFX graphics services and a pointer to this interface is provided to the graphics virtual channel in the <a href="/windows/desktop/api/wrdsgraphicschannels/nf-wrdsgraphicschannels-iwrdsgraphicschannel-open">IWRdsGraphicsChannel::Open</a> method.

## -inheritance

The <b>IWRdsGraphicsChannelEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWRdsGraphicsChannelEvents</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/wrdsgraphicschannels/nf-wrdsgraphicschannels-iwrdsgraphicschannel-open">IWRdsGraphicsChannel::Open</a>
