---
UID: NN:tsvirtualchannels.IWTSListener
title: IWTSListener (tsvirtualchannels.h)
description: Manages configuration settings for each listener for the dynamic virtual channel (DVC) connection.
helpviewer_keywords: ["IWTSListener","IWTSListener interface [Remote Desktop Services]","IWTSListener interface [Remote Desktop Services]","described","termserv.iwtslistener","tsvirtualchannels/IWTSListener"]
old-location: termserv\iwtslistener.htm
tech.root: TermServ
ms.assetid: af0dda9a-0d18-4f44-ac13-0bf2b903d34e
ms.date: 12/05/2018
ms.keywords: IWTSListener, IWTSListener interface [Remote Desktop Services], IWTSListener interface [Remote Desktop Services],described, termserv.iwtslistener, tsvirtualchannels/IWTSListener
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
 - IWTSListener
 - tsvirtualchannels/IWTSListener
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
 - IWTSListener
---

# IWTSListener interface


## -description

Manages configuration settings for each listener for the dynamic virtual channel (DVC) connection.

This interface is implemented by the Remote Desktop Connection (RDC) client. A reference is kept typically by the Remote Desktop Connection (RDC) client plug-in. The methods can be executed in any thread that the plug-in chooses. An instance is retrieved by calling the <a href="/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener">IWTSVirtualChannelManager::CreateListener</a> method.

## -inheritance

The <b>IWTSListener</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWTSListener</b> also has these types of members:

